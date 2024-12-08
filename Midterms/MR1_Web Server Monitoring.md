![image](https://github.com/user-attachments/assets/dd4d3510-9aa3-4340-bf42-2cb1765558a8)


# SYSADM1 -- Web Server Monitoring

1.  How do you monitor web server statistics?

> We can monitor a Windows web server by using tools like Windows
> Performance Monitor (PerfMon), which allows you to track metrics such
> as CPU, memory, disk I/O, and network usage in real-time. Event Viewer
> is another built-in tool that logs system and application events,
> including web server issues. Also, third-party solutions like
> SolarWinds or Zabbix offer advanced real-time monitoring,
> notifications, and detailed analysis of web server health and
> performance.
>
> For web traffic specifically, monitoring IIS (Internet Information
> Services) logs helps track the number of hits, client IP addresses,
> and status codes of responses for detailed insights into web activity.

2.  What are the key metrics that you need to monitor in a web server?

-   Average Response Time -- time the server takes to process and
    respond to a request. High times indicate performance issues.

-   Requests per Second -- the number of requests the server handles
    each second, showing its load and capacity.

-   Memory Usage -- the amount of RAM used. High usage can indicate
    overload or memory leaks.

-   Error Rate -- the percentage of failed requests (e.g., 4xx, 5xx
    errors). High rates suggest server or app issues.

-   Common Error Types - frequent errors that help troubleshoot broken
    links or server issues.

-   CPU Utilization -- it shows if the CPU is maxed out, signaling heavy
    load or inefficiencies.

-   Disk I/O -- this measures storage read/write operations to check for
    bottlenecks.

3.  Analyze the provided web server statistics to determine what is
    being asked for below.

![image](https://github.com/user-attachments/assets/3f7b3be0-5e03-42fb-a36f-ac508a17f8b4)


A.  Average response time: 738.89 ms

B.  Request per second: 1 request per second

C.  Memory usage: Minimum -- 30MB

> Maximum -- 200MB
>
> Average -- 97.78MB

D.  Error rate: 22.2222%

E.  Common error types: 404 Not Found (1 instance)

> 500 Internal Server Error (1 instance)

4.  What are the possible issues in the web server statistics above?

-   The POST request to /contact has a very high response time of 5000
    ms, which is much higher than others, indicating a performance
    issue.

-   An error rate of 22.22% could be concerning, with one 404 error
    (maybe a broken link) and one 500 error (indicating a server-side
    issue).

-   The memory usage is highest for the POST request to /contact (200
    MB), suggesting that this request is consumes a lot of resources and
    could be linked to the high response time.

**Grading Rubric**

![image](https://github.com/user-attachments/assets/2634e0f9-0391-448b-879c-e2ef4e68e3cd)

