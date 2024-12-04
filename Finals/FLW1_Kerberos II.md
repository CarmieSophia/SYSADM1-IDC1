+-------------------------------+---------------------------+----------+
| ![](vertopal_fecb78           |                           |          |
| 5790f24736bcee400942d91782/me |                           |          |
| dia/image1.png){width="2.4in" |                           |          |
| h                             |                           |          |
| eight="0.5881944444444445in"} |                           |          |
|                               |                           |          |
| SCHOOL OF INFORMATION AND     |                           |          |
| TECHNOLOGY                    |                           |          |
+-------------------------------+---------------------------+----------+
| NAME: **OLIVAS, CARMIE SOPHIA | DATE PERFORMED: **13 NOV  | /50      |
| N.**                          | 2024**                    |          |
+-------------------------------+---------------------------+----------+
| Section: **IDC1**             | DATE SUBMITTED: **13 NOV  |          |
|                               | 2024**                    |          |
+-------------------------------+---------------------------+----------+

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

*bash*

*sudo apt update && sudo apt upgrade --y*

![](vertopal_fecb785790f24736bcee400942d91782/media/image2.png){width="5.232758092738408in"
height="4.3733005249343835in"}

![](vertopal_fecb785790f24736bcee400942d91782/media/image3.png){width="5.237813867016623in"
height="3.957734033245844in"}

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y*

![](vertopal_fecb785790f24736bcee400942d91782/media/image4.png){width="4.727998687664042in"
height="3.5309306649168852in"}

![](vertopal_fecb785790f24736bcee400942d91782/media/image5.png){width="4.872338145231846in"
height="3.5207567804024498in"}

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y*

![](vertopal_fecb785790f24736bcee400942d91782/media/image6.png){width="4.955108267716535in"
height="3.7651771653543307in"}*\
*![](vertopal_fecb785790f24736bcee400942d91782/media/image7.png){width="4.897900262467192in"
height="3.633131014873141in"}

-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

ini

\[libdefaults\]

default_realm = MYLAB.LOCAL

\[realms\]

MYLAB.LOCAL = {

kdc = \<VM1_IP_or_hostname\>

admin_server = \<VM1_IP_or_hostname\>

}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

![](vertopal_fecb785790f24736bcee400942d91782/media/image9.png){width="4.974641294838145in"
height="3.7121773840769903in"}

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

![](vertopal_fecb785790f24736bcee400942d91782/media/image11.png){width="4.7965507436570425in"
height="3.8636909448818897in"}

3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*

![](vertopal_fecb785790f24736bcee400942d91782/media/image12.png){width="5.548211942257218in"
height="4.531122047244095in"}

**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

![](vertopal_fecb785790f24736bcee400942d91782/media/image13.png){width="4.51490813648294in"
height="0.9592104111986002in"}

2.  **Verify the User Principal:**

    -   

    -   To confirm the principal is created, list all principals:

*sudo kadmin.local -q \"listprincs\"*

![](vertopal_fecb785790f24736bcee400942d91782/media/image14.png){width="5.095793963254593in"
height="2.4066404199475064in"}

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

![](vertopal_fecb785790f24736bcee400942d91782/media/image15.png){width="5.3848665791776025in"
height="4.006587926509186in"}

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set o

-   

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit* *testuser@MYLAB.LOCAL*

![](vertopal_fecb785790f24736bcee400942d91782/media/image16.png){width="4.885442913385827in"
height="3.6668580489938756in"}

-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*list*

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
