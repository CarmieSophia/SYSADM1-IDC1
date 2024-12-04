
![image](https://github.com/user-attachments/assets/2c75b347-c0a2-44d4-bc1d-030b3e01919c)



# SYSADM1 -- CAPACITY MANAGEMENT & PLANNING

### Part 1. A Simulated Dataset for Capacity Planning Exercise

![image](https://github.com/user-attachments/assets/8fc3415c-9c85-45ed-abc9-9badf69d19ed)

**Scenario:** A mid-sized e-commerce
website is expecting a significant surge in traffic due to an upcoming
holiday sale.

**Projected Traffic Increase**

-   Expected Peak Traffic: **5x the normal peak traffic**

-   Peak Time: **12:00 PM - 3:00 PM on the sale day**

**System Specifications**

-   Server Count: **5**

-   CPU Cores per Server: **8**

-   RAM per Server: **32GB**

-   Network Bandwidth per Server: **1Gbps**

**Additional Considerations**

-   New Product Launch: **A highly anticipated product will be released
    during the sale.**

-   Marketing Campaign: **A major marketing campaign will be launched to
    promote the sale.**

-   Potential Cyber Threats: **Increased traffic can attract malicious
    actors.**

**Tasks:**

1.  Review the provided server performance data and identify potential
    bottlenecks

-   Server Overload Limited CPU and RAM resources on existing servers.
    Network bandwidth constraints (1Gbps per server).

-   Increased Risk of Cyber Threats: The event could attract malicious
    activities like DDoS attacks.

-   Inefficient Handling of New Product Launch: High interest in the
    anticipated product may lead to traffic spikes beyond expectations.

**2.  Brainstorm possible solutions to address the identified bottlenecks.
    Propose potential solutions considering hardware and software-based
    solutions.**

**3.  Discuss the pros and cons of each proposed solution by filling out
    the table below.**

![image](https://github.com/user-attachments/assets/b56bc7a7-fc68-46ac-a91a-78ca778da90a)


**Grading Rubric:**

![image](https://github.com/user-attachments/assets/5537ba8b-add3-480f-a4be-be19ff9bcf58)



### Part 2. Network Scalability Analysis

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/48c05018-1ac7-447c-8dc5-b3d1e6765ed5)


**NETWORK ANALYSIS**

**Bottlenecks:**

-   The single Edge Router can become a bottleneck as all traffic to and
    from the Internet passes through it.

-   The core switch handles inter-VLAN routing and connects to all
    VLANs. If it is overloaded or fails, the entire network is
    disrupted.

**Security Risks**

-   Lack of a visible firewall between the edge router and the internet,
    increasing exposure to external threats.

-   No indication of VLAN-specific security configurations (e.g., ACLs
    or segmentation rules) to isolate and secure traffic.

-   Servers in each VLAN might be vulnerable if no endpoint security is
    implemented.

**Capacity Limitations:**

-   The Layer 2 switches are directly connected to multiple servers,
    which could lead to bandwidth congestion if high traffic is
    sustained.

-   The core switch\'s throughput and port capacity might be inadequate
    if the network grows significantly.
    

**SCALABILITY PLANNING**

**Proposed Solutions**

> **Add Redundancy**

-   Introduce a secondary core switch for high availability using
    protocols like VRRP or HSRP.

-   Implement link aggregation (LACP) between the core switch and Layer
    2 switches for load balancing and fault tolerance.

> **Increase Bandwidth Capacity**

-   Upgrade links between the core switch and Layer 2 switches to 10Gbps
    connections if not already configured.

-   Implement QoS to prioritize traffic (e.g., application traffic over
    bulk file transfers).

> **Enhance Security:**

-   Deploy a firewall between the edge router and the internet.

-   Use VLAN-based security policies and configure ACLs to control
    inter-VLAN traffic.

-   Segment sensitive servers into isolated VLANs with restricted
    access.

> **Prepare for Growth**

-   Use modular core switches that can support additional ports and
    higher speeds.

-   Evaluate cloud-hosted solutions for server scalability if physical
    server expansion becomes impractical.
    

**EVALUATION OF SOLUTIONS**

> **ISP Redundancy**

-   The dual ISP setup ensures that if one ISP experiences an outage or
    decline in performance, the other can take over, providing
    uninterrupted internet access. This redundancy will minimize the
    risk of downtime, which is important for maintaining continuous
    business operations & service.

> **Core Switches**

-   Adding a second core switch introduces high availability and fault
    tolerance within the network. By implementing technologies such as
    HSRP (Hot Standby Router Protocol), the network can seamlessly
    switch between core switches in case one fails, avoiding network
    disruptions. The two core switches also help distribute the network
    load, improving overall network performance.

> **Edge Routers**

-   The inclusion of two edge routers provides redundancy at the
    network's entry and exit points, making sure that internal network
    traffic can still access external services in case of a failure.
    This redundancy is crucial for maintaining both internet
    connectivity and security. Like with core switches, protocols such
    as HSRP should be used to manage failover and ensure seamless
    operation.

**Overall Evaluation**

-   The addition of these devices significantly improves the network's
    fault tolerance, ensuring high availability and minimal downtime.
    However, they also increase the complexity of the network, requiring
    careful management of redundancy protocols and configurations.
    Proper monitoring and management tools might be necessary to ensure
    that all devices work cohesively to provide optimal performance and
    failover.


**PROPOSED DESIGN**

![image](https://github.com/user-attachments/assets/96bbc6b3-e2cc-4c0b-857d-e97510688768)


#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### 

#### **EVALUATION & JUSTIFICATION**

-   A firewall was added between the edge router and the internet, a
    redundant core switch for failover and load balancing.

-   VLAN-specific policies shown openly with sensitive servers isolated
    in different VLANs.

-   10Gbps uplinks between switches.

The proposed design includes the addition of two ISPs to ensure greater reliability and redundancy for internet connectivity. This dual-ISP setup lessens the risk of a single point of failure, providing continuous internet access even if one ISP encounters issues. Redundancy is also implemented across all critical devices, including two core switches and two edge routers. This redundant design ensures high availability and fault tolerance which prevents network downtime in case of device failure. By incorporating these redundant elements, the network is made more robust, maintaining service continuity and improving overall network reliability. 

                  
![image](https://github.com/user-attachments/assets/aa87f5c0-96a3-4ea4-a749-d0d2766c9d2e)

