+------------------------------+----------------------------+----------+
| ![](vertopal_21d0cf3b        |                            |          |
| 95cd492ba16253fb7782b253/med |                            |          |
| ia/image1.png){width="2.4in" |                            |          |
| he                           |                            |          |
| ight="0.5881944444444445in"} |                            |          |
|                              |                            |          |
| SCHOOL OF INFORMATION AND    |                            |          |
| TECHNOLOGY                   |                            |          |
+------------------------------+----------------------------+----------+
| NAME: **OLIVAS, CARMIE       | DATE PERFORMED: **16 OCT   | /50      |
| SOPHIA N.**                  | 2024**                     |          |
+------------------------------+----------------------------+----------+
| Section: **IDC1**            | DATE SUBMITTED: **16 OCT   |          |
|                              | 2024**                     |          |
+------------------------------+----------------------------+----------+

# SYSADM1 -- Setting Up Webserver

# Requirement: 

-   A virtual machine running Linux and Windows OS

    Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

    ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image2.png){width="5.667998687664042in"
    height="4.644633639545057in"}

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image3.png){width="5.776270778652669in"
        height="4.72878937007874in"}

3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image4.png){width="4.889695975503062in"
        height="4.002988845144357in"}

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image5.png){width="3.652083333333333in"
        height="1.52377624671916in"}\<

    -   Save it as default.html or your preferred name.\
        \
        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image6.png){width="4.721675415573054in"
        height="3.8654385389326333in"}

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image7.png){width="7.027083333333334in"
        height="3.2090277777777776in"}

        ![](vertopal_21d0cf3b95cd492ba16253fb7782b253/media/image8.png){width="7.027083333333334in"
        height="3.2868055555555555in"}

        Grading Rubric

  ------------------------------------------------------------------------------
  **Criteria**      **Points**   **Description**
  ----------------- ------------ -----------------------------------------------
  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ------------------------------------------------------------------------------
