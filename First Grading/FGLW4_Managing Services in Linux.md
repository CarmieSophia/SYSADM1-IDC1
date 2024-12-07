+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 2f16a6e27ead41fbbf2f2fe65d4f390d |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: **OLIVAS, CARMIE SOPHIA    | DATE PERFORMED: **11   |          |
| N.**                             | SEPT 2024**            |          |
+----------------------------------+------------------------+----------+
| Section: **IDC1**                | DATE SUBMITTED: **11   |          |
|                                  | SEPT 2024**            |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service ---status-all command to list all active and
    inactive services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils                             anarcon

  cups                                   bluetooth

  dbus                                   cryptdisks

  openvpn                                plymouth

  sysstat                                speech-=dispatcher
  -----------------------------------------------------------------------

SS:

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image3.png){width="6.693378171478566in"
height="6.016037839020123in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image4.png){width="4.359946412948381in"
height="1.1875in"}

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image5.png){width="6.207677165354331in"
height="0.9936209536307962in"}

3.  Check the status of the Bluetooth service. What is its status?

***The status is Active.***

SS:

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image6.png){width="5.858442694663167in"
height="5.017649825021873in"}

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image7.png){width="6.356969597550306in"
height="4.829136045494313in"}

4.  Check the status of the cups services. Since when was it running?

***It was already active and running when I issued the service
--status-all command at the beginning.***

SS:

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image8.png){width="6.077567804024497in"
height="5.7009853455818025in"}

5.  Stop cups services.

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image9.png){width="6.725554461942258in"
height="0.6719575678040245in"}

6.  Verify if the service was stopped.

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image10.png){width="6.594395231846019in"
height="5.901002843394576in"}

7.  Restart the cups services

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image11.png){width="4.344355861767279in"
height="0.28128937007874016in"}

8.  Verify if the service was restarted.

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image12.png){width="6.329646762904637in"
height="5.71615813648294in"}

![](vertopal_2f16a6e27ead41fbbf2f2fe65d4f390d/media/image13.png){width="6.245592738407699in"
height="2.59168416447944in"}
