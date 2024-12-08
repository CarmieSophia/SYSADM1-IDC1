+-------------------------------+---------------------------+----------+
| ![](vertopal_0248e1           |                           |          |
| 986a6f439cb852b4eb50bc8d8d/me |                           |          |
| dia/image1.png){width="2.4in" |                           |          |
| h                             |                           |          |
| eight="0.5881944444444445in"} |                           |          |
|                               |                           |          |
| SCHOOL OF INFORMATION AND     |                           |          |
| TECHNOLOGY                    |                           |          |
+-------------------------------+---------------------------+----------+
| NAME: **OLIVAS, CARMIE SOPHIA | DATE PERFORMED: **25 SEPT | /50      |
| N.**                          | 2024**                    |          |
+-------------------------------+---------------------------+----------+
| Section: **IDC1**             | DATE SUBMITTED: **25 SEPT |          |
|                               | 2024**                    |          |
+-------------------------------+---------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image2.png){width="6.361907261592301in"
> height="3.7747692475940506in"}

2.  Connect one client to the recently created domain\
    ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image3.png){width="6.281421697287839in"
    height="3.219235564304462in"}

3.  Install Print Services Role:

> ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image4.png){width="6.3101399825021876in"
> height="2.6951695100612425in"}

4.  Search the internet for any printer installer and convert it to iso

5.  

6.  ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image5.png){width="7.027083333333334in"
    height="3.0069444444444446in"}Install and deploy it as network
    printer

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

> ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image6.png){width="5.899847987751531in"
> height="4.521525590551181in"}\
> ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image6.png){width="6.0528652668416445in"
> height="4.638794838145232in"}

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   ![](vertopal_0248e1986a6f439cb852b4eb50bc8d8d/media/image7.png){width="7.027083333333334in"
        height="4.9375in"}Monitor performance metrics related to print
        services.

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

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------
