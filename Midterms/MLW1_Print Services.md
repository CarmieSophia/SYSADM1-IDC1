![image](https://github.com/user-attachments/assets/e4e27bf5-2855-4918-81e1-f43197e81048)


# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![image](https://github.com/user-attachments/assets/c7e17897-541c-4f9c-b468-e63676f00cae)


2.  Connect one client to the recently created domain\
> ![image](https://github.com/user-attachments/assets/b9406273-fe72-4790-8f36-08cf53609382)


3.  Install Print Services Role:

> ![image](https://github.com/user-attachments/assets/8f19284b-723f-4a88-b1a1-bf2daa580e9b)


4.  Search the internet for any printer installer and convert it to iso
 

5.  Install and deploy it as network printer
> ![image](https://github.com/user-attachments/assets/9d365f95-2304-46aa-b490-652d0630ad25)


Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

> ![image](https://github.com/user-attachments/assets/d29fc53f-7d25-4de1-887f-72fa2f2b6d04)
> ![image](https://github.com/user-attachments/assets/fb22e06a-8316-459d-9d53-a3727c31cd08)


2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   > ![image](https://github.com/user-attachments/assets/7efd66b1-6002-4fe3-b8ec-1a8c3c5c5bb5)


3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

### 1. PrinterLogic

> Features:

-   Allows print management without the need for traditional print
    servers.

-   Automatically installs and updates printer drivers on client
    machines.

-   Users can add printers through a web interface, reducing IT
    workload.

-   Offers options for secure print release, ensuring sensitive
    documents are only printed when the user is present.

-   Provides insights into printer usage, costs, and environmental
    impact.

> Pricing:

-   Pricing is typically subscription-based, and the cost can vary based
    on the number of users and printers.

-   Offers tiered pricing based on features selected, which can be
    customized according to organizational needs.

> Compatibility:

-   Fully compatible with Windows Server 2019 and supports various
    printer brands and models.

2\. PaperCut

> Features:

-   Monitors print jobs in real-time, collecting data on usage metrics
    (page counts, color vs. black and white).

-   Enables organizations to charge users for printing, including
    setting quotas and limits.

-   Allows detailed permissions and access control for different user
    groups.

-   Extensive reporting tools to analyze print usage and costs.

-   Users must authenticate at the printer to retrieve their print jobs,
    enhancing document security.

> Pricing:

-   Offers a one-time licensing fee for its software, with additional
    costs for optional features (e.g., advanced reporting).

-   Pricing varies depending on the number of users and printers, with a
    free trial available for evaluation.

> Compatibility:

-   Fully compatible with Windows Server 2019 and supports a wide range
    of printer models from various manufacturers.

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).



  
