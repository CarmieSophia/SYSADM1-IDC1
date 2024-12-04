![image](https://github.com/user-attachments/assets/042e5871-de8a-4e75-9937-f56164f72b9d)

# SYSADM1 -- Kerberos Basics

Research Activity

1.  **What is Kerberos, and why is it used?**

> Kerberos is a network authentication protocol that uses secret-key
> cryptography to provide secure communication over unsecured networks.
> It was created at MIT and is mainly used to confirm the legitimacy of
> users and services on a network, lowering the dangers involved in
> sending passwords over networks. Kerberos is frequently used to
> authenticate service requests between trustworthy hosts over untrusted
> networks, including the internet, in high-security settings like
> corporate intranets. The protocol is a strong option for safe,
> cross-platform authentication because it is compatible with most major
> operating systems, such as Microsoft Windows, Apple macOS, FreeBSD,
> and Linux.

2.  **What are the main components of Kerberos?**

![image](https://github.com/user-attachments/assets/c340878f-4191-475f-9432-a74c80ddb135)


3.  What is a \"ticket\" in Kerberos, and why is it important?

> An encrypted data packet known as a \"ticket\" in Kerberos is used to
> verify a user\'s identity on a network. A ticket, which is issued by
> the Key Distribution Center (KDC), enables customers to safely access
> services without having to submit passwords over the network
> frequently. To guarantee that it can only be used by the verified user
> and during a predetermined window of time, the ticket is time-stamped
> and encrypted. Tickets ensure that authentication happens
> transparently and securely once the user is initially authenticated.
> It is important because:

-   Minimizes Password Exposure

-   Prevents Replay Attacks

-   Enhanced Security

-   Secure and Streamlined Authentication which reduces of repeated
    log-ins

4.  What is a Kerberos \"realm,\" and what is its purpose?

> Realm is an administrative domain where the Key Distribution Center
> (KDC) manages and authenticates all users and services within its
> scope. Kerberos-using resources and identities can be logically
> grouped into Kerberos realms. Your Kerberos identity and your gateway
> to the Kerberos-controlled network resources are located in your
> realm. Realms are referred to as domains in Windows. In Kerberos, a
> realm is used to create a trusted administrative domain for user and
> service management and authentication. All authentication procedures
> are safely managed by the Key Distribution Center (KDC) within a
> realm. Additionally, realms facilitate safe communication between
> domains by enabling cross-realm authentication, which permits users in
> one realm to access resources in another trustworthy realm.

5.  How does Kerberos authenticate a user?

> Kerberos stores the specific ticket for each session on the
> end-user\'s device. Instead of a password, a Kerberos-aware service
> looks for this ticket. Kerberos authentication takes place in a
> Kerberos realm, an environment in which a KDC is authorized to
> authenticate a service, host, or user.
>
> **PROCESS ON HOW TO AUTHENTICATE A USER**

-   The client sends a request to the Authentication Server (AS).

-   The AS verifies the client's credentials and issues a Ticket
    Granting Ticket (TGT).

-   When the client needs access to a specific service, it presents the
    TGT to the Ticket Granting Server (TGS).

-   The TGS issues a service ticket, which the client then uses to
    access the service.

> ![image](https://github.com/user-attachments/assets/dad2b2ee-a1bd-4df1-a679-536f399d890a)


6.  What does each component (KDC, TGS, AS) contribute to the
    authentication process?

> ![image](https://github.com/user-attachments/assets/080eefc8-85b6-475e-92cb-3569da7075b0)


7.  How does a ticket improve security compared to repeated password
    logins?

Users may safely access services without having to continually input
their passwords thanks to tickets, which are encrypted data packets used
for authentication. The ticket acts as identification once a user has
been validated, guaranteeing safe, time-bound access to network
services.

On how to Improve Security is:

-   **No Repeated Password Entry**: Tickets allow users to access
    multiple services without entering passwords each time, reducing the
    risk of interception.

-   **Encryption:** Tickets are encrypted, ensuring that only the
    intended user can use them, preventing unauthorized access.

-   **Reduced Attack Vectors:** By using tickets instead of transmitting
    passwords, the risk of interception and password-based attacks is
    minimized.

-   **Prevents Replay Attacks:** Each ticket is valid only for a limited
    time, making it useless if intercepted after its expiration.

-   **Centralized Authentication Control:** The Key Distribution Center
    (KDC) manages the issuance and validation of tickets


**REFERENCES:**

*Kerberos Terminology*. (n.d.).
<https://web.mit.edu/kerberos/kfw-4.1/kfw-4.1/kfw-4.1-help/html/kerberos_terminology.htm#:~:text=Kerberos%20realms%20are%20a%20way,Windows%2C%20realms%20are%20called%20domains>.

Loshin, P., & Cobb, M. (2021, September 15). *Kerberos*. Security.
<https://www.techtarget.com/searchsecurity/definition/Kerberos>

*What is Kerberos? Kerberos authentication explained \| Fortinet*.
(n.d.). Fortinet.
<https://www.fortinet.com/resources/cyberglossary/kerberos-authentication#:~:text=During%20authentication%2C%20Kerberos%20stores%20the,service%2C%20host%2C%20or%20user>.

*IBM SPSS Collaboration and Deployment Services*. (n.d.).
<https://www.ibm.com/docs/en/sc-and-ds/8.4.0?topic=concepts-kerberos-ticket>
