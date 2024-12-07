+--------------------------------+--------------------------+----------+
| ![](vertopal_382c              |                          |          |
| 1193af4e47a780860273d80875a3/m |                          |          |
| edia/image1.png){width="2.4in" |                          |          |
| height="0.5881944444444445in"} |                          |          |
|                                |                          |          |
| SCHOOL OF INFORMATION AND      |                          |          |
| TECHNOLOGY                     |                          |          |
+--------------------------------+--------------------------+----------+
| NAME: **OLIVAS, CARMIE SOPHIA  | DATE PERFORMED: **28 AUG |          |
| N.**                           | 2024**                   |          |
+--------------------------------+--------------------------+----------+
| Section: **IDC1**              | DATE SUBMITTED: **28 AUG |          |
|                                | 2024**                   |          |
+--------------------------------+--------------------------+----------+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image2.png){width="5.697834645669292in"
> height="4.19215113735783in"}

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  ---------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of        **Screenshot**
               Service**        
  ------------ ---------------- ---------------------------------------------------------------------------------------------
  Start        IP Helper        ![](vertopal_382c1193af4e47a780860273d80875a3/media/image3.png){width="4.567317366579178in"
                                height="3.6460903324584426in"}

  Stop         IP Helper        ![](vertopal_382c1193af4e47a780860273d80875a3/media/image4.png){width="4.569295713035871in"
                                height="3.655345581802275in"}

  Restart      IP Helper        ![](vertopal_382c1193af4e47a780860273d80875a3/media/image5.png){width="4.876852580927384in"
                                height="3.886926946631671in"}

  Pause        Microsoft .NET   ![](vertopal_382c1193af4e47a780860273d80875a3/media/image6.png){width="4.914023403324585in"
               Framework NGEN   height="3.915582895888014in"}
               v2.0.50727_X64   
  ---------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image7.png){width="5.379790026246719in"
> height="4.298942475940508in"}
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image8.png){width="5.2489982502187225in"
> height="4.145664916885389in"}
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image9.png){width="5.271353893263342in"
> height="4.208122265966754in"}
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image10.png){width="5.036713692038496in"
> height="4.034248687664042in"}
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image11.png){width="5.059564741907262in"
> height="4.05705271216098in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image12.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"\<path\>\" start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image13.png){width="5.2739337270341204in"
> height="4.30295384951881in"}
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image14.png){width="5.238423009623797in"
> height="3.897626859142607in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_382c1193af4e47a780860273d80875a3/media/image15.png){width="5.390600393700788in"
> height="4.3054494750656165in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **50 /50**                                         
  ---------------------------------------------------------------------------------------
