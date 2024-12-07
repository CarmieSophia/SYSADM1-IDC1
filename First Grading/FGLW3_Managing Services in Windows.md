![image](https://github.com/user-attachments/assets/ff3ed800-94c8-440d-9398-56b57ecb4ac1)


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

> ![image](https://github.com/user-attachments/assets/438ac4bf-471a-4a3a-a3d3-079444dd6dad)


2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

> ![image](https://github.com/user-attachments/assets/d22fbfaf-2eeb-4b2f-988b-d24750102fbd)
> ![image](https://github.com/user-attachments/assets/d2a6a95a-be3e-43ed-8213-c5d1cbc6c5bf)
> ![image](https://github.com/user-attachments/assets/f430bfc1-7d30-4d91-870f-e7cc44056bfb)
> ![image](https://github.com/user-attachments/assets/b38cc587-cdc9-4dad-90cc-675cea692de4)



4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> ![image](https://github.com/user-attachments/assets/e6d0ca98-1312-4292-8638-05e226fa420e)
> ![image](https://github.com/user-attachments/assets/e26ce538-0219-4826-b515-ab5df7ca3dd9)
> ![image](https://github.com/user-attachments/assets/9bc13a01-a887-466d-99ce-8dffe0f8b468)
> ![image](https://github.com/user-attachments/assets/bf10ce0c-09a1-49ae-bebe-3f1b4591d3b6)
> ![image](https://github.com/user-attachments/assets/292e6d45-46cb-46c1-96a3-5654f813a242)


5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.
> ![image](https://github.com/user-attachments/assets/e7045dad-4641-4a68-87b5-09844603e8c4)

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
> ![image](https://github.com/user-attachments/assets/e9876537-65c6-4567-9769-906a04a18b9f)
> ![image](https://github.com/user-attachments/assets/609ac0c9-bdc4-480a-927b-7393727c8716)


10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![image](https://github.com/user-attachments/assets/d1d04e10-9bf7-46a0-88c1-d08cbc006d95)


**Rubric**

![image](https://github.com/user-attachments/assets/57f28fc3-c187-49e1-8a38-db6214cfb1d7)

