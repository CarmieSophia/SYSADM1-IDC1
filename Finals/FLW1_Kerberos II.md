![image](https://github.com/user-attachments/assets/d5f3e876-5420-499c-968f-087228bfa628)

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

## **Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

## **Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

## **Step 1: Initial Setup and Package Installation**

### 1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

> *bash*
> *sudo apt update && sudo apt upgrade --y*

> ![image](https://github.com/user-attachments/assets/e98eeacc-7637-440d-b104-298b59acbe4f)
> ![image](https://github.com/user-attachments/assets/74748ba7-fc0d-47f4-ab20-53145cf35fff)


### 2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

> *bash*
> *sudo apt install krb5-kdc krb5-admin-server --y*

> ![image](https://github.com/user-attachments/assets/51931b46-3951-4f53-904f-7646a0b20c13)
> ![image](https://github.com/user-attachments/assets/e955c3f1-286d-467a-ab5d-834227c0bf66)


### 3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

> *bash*
> *sudo apt install krb5-user --y*

> ![image](https://github.com/user-attachments/assets/2af9967e-3bd8-42e8-9fe8-9fc62f5af2f0)
> ![image](https://github.com/user-attachments/assets/b66f9dc5-415a-4f6d-a437-a11d293dd593)


    -   During installation, when prompted, enter the Kerberos realm you plan to set up, e.g., MYLAB.LOCAL.

## Step 2: Configure the Kerberos Server (VM1)**

### 1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

> *bash*
> *sudo nano /etc/krb5.conf*

    -   Set the realm as MYLAB.LOCAL. You should also specify the KDC and admin server as VM1's hostname or IP address:

    ini
    
    \[libdefaults\]
    
    default_realm = MYLAB.LOCAL
    
    \[realms\]
    
    MYLAB.LOCAL = {
    
    kdc = \<VM1_IP_or_hostname\>
    
    admin_server = \<VM1_IP_or_hostname\>

}

    -   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

> ![image](https://github.com/user-attachments/assets/726e4eea-431e-4cf0-b526-c19589a8ef42)


### 2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

> *sudo systemctl enable krb5-admin-server*
*bash*

> *sudo systemctl enable krb5-admin-server*
*sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

> ![image](https://github.com/user-attachments/assets/b3220814-156c-4f92-a6f0-7f07a5f6533c)


### 3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

> *bash*

> *sudo systemctl start krb5-kdc*

> *sudo systemctl start krb5-admin-server*

> *sudo systemctl enable krb5-kdc*

> *sudo systemctl enable krb5-admin-server*

> ![image](https://github.com/user-attachments/assets/bd60ee7f-be2a-4a5b-8cee-33d429f41bd6)


## **Step 3: Set Up a Kerberos User Principal**

### 1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

> *sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

    -   Set a password for testuser.

> ![image](https://github.com/user-attachments/assets/53fa2b15-f4e1-4b71-ac84-c8f637fc634e)


### 2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

> *sudo kadmin.local -q \"listprincs\"*

> ![image](https://github.com/user-attachments/assets/14548171-aa72-40c3-a41f-c0582dc4f867)


## **Step 4: Configure the Kerberos Client (VM2)**

### 1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

> *bash*

> *sudo nano /etc/krb5.conf*

> ![image](https://github.com/user-attachments/assets/228c05db-8b1a-4ca7-b246-e140b236fab4)


    -   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set o
  

## **Step 5: Test Kerberos Authentication**

### 1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

> *bash*

> *kinit* *testuser@MYLAB.LOCAL*

> ![image](https://github.com/user-attachments/assets/883699f5-5114-4bf5-b63b-414312e925f8)


    -   Enter the password you set for testuser.

### 2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*list*

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
