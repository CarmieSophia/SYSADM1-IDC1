+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 9cd268d27e3f47da9dc851aec016c912 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+==================================+========================+==========+
| NAME:                            | DATE PERFORMED: **26   | /50      |
|                                  | NOV 2024**             |          |
| **BUSONGAN, DEMIRAYE-ANNE**      |                        |          |
|                                  |                        |          |
| **OLIVAS, CARMIE SOPHIA N.**     |                        |          |
+----------------------------------+------------------------+----------+
| Section: **IDC1**                | DATE SUBMITTED: **26   |          |
|                                  | NOV 2024**             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- CAPACITY MANAGEMENT & PLANNING

## Part 1. A Simulated Dataset for Capacity Planning Exercise {#part-1.-a-simulated-dataset-for-capacity-planning-exercise .list-paragraph}

![](vertopal_9cd268d27e3f47da9dc851aec016c912/media/image2.png){width="4.416666666666667in"
height="2.3055555555555554in"}**Scenario:** A mid-sized e-commerce
website is expecting a significant surge in traffic due to an upcoming
holiday sale.

### **[Projected Traffic Increase]{.underline}**

-   Expected Peak Traffic: **5x the normal peak traffic**

-   Peak Time: **12:00 PM - 3:00 PM on the sale day**

### **[System Specifications]{.underline}**

-   Server Count: **5**

-   CPU Cores per Server: **8**

-   RAM per Server: **32GB**

-   Network Bandwidth per Server: **1Gbps**

### **[Additional Considerations]{.underline}**

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

2.  Brainstorm possible solutions to address the identified bottlenecks.
    Propose potential solutions considering hardware and software-based
    solutions.

3.  Discuss the pros and cons of each proposed solution by filling out
    the table below.

+---------+---------+----------+------------+------------+------------+
| **P     | *       | **CONS** | *          | **CO       | *          |
| ROPOSED | *PROS** |          | *ESTIMATED | MPLEXITY** | *POTENTIAL |
| SOL     |         |          | COST       |            | IMPACT ON  |
| UTION** |         |          | (USD)**    |            | SYSTEM     |
|         |         |          |            |            | PER        |
|         |         |          |            |            | FORMANCE** |
+=========+=========+==========+============+============+============+
| **Add   | In      | High     | ₱280,000   | Medium:    | S          |
| More    | creases | upfront  | --₱840,000 | Requires   | ignificant |
| Se      | c       | cost.    | per server | pr         | i          |
| rvers** | apacity |          |            | ocurement, | mprovement |
|         | for     | Setup    |            | ins        | in         |
|         | t       | and      |            | tallation, | handling   |
|         | raffic. | de       |            | and        | traffic    |
|         |         | ployment |            | con        | spikes but |
|         | S       | may take |            | figuration | may not    |
|         | calable | time.    |            | of         | address    |
|         | for     |          |            | additional | bandwidth  |
|         | future  |          |            | servers.   | l          |
|         | growth. |          |            |            | imitations |
|         |         |          |            |            | ef         |
|         |         |          |            |            | fectively. |
+---------+---------+----------+------------+------------+------------+
| *       | F       | Requires | ₱56        | High:      | D          |
| *Enable | lexible | initial  | ,000--₱168 | Involves   | ynamically |
| Auto-   | and     | setup    | ,000/month | c          | adapts to  |
| Scaling | c       | and      | (us        | onfiguring | traffic    |
| in      | ost-eff | testing. | age-based) | au         | needs,     |
| Cloud** | icient. |          |            | to-scaling | ensuring   |
|         |         | De       |            | rules,     | minimal    |
|         | Quickly | pendency |            | monitoring | downtime,  |
|         | adjusts | on cloud |            | tools, and | and        |
|         | to      | p        |            | ensuring   | handles    |
|         | demand. | rovider. |            | cloud      | unexpected |
|         |         |          |            | platform   | spikes     |
|         |         |          |            | comp       | ef         |
|         |         |          |            | atibility. | ficiently. |
+---------+---------+----------+------------+------------+------------+
| **O     | Cost-ef | Limited  | ₱28,00     | Low:       | Minor      |
| ptimize | fective | imp      | 0--₱56,000 | Simple     | im         |
| Current | so      | rovement | (software  | tasks like | provements |
| Se      | lution. | c        | updates    | tweaking   | through    |
| rvers** |         | apacity. | /upgrades) | server     | load       |
|         | Uses    |          |            | settings,  | balancing, |
|         | e       | Might    |            | installing | cache      |
|         | xisting | not      |            | updates,   | opt        |
|         | res     | fully    |            | or adding  | imization, |
|         | ources. | handle   |            | small      | and        |
|         |         | 5x       |            | hardware   | upgrading  |
|         |         | traffic. |            | upgrades.  | specific   |
|         |         |          |            |            | hardware   |
|         |         |          |            |            | c          |
|         |         |          |            |            | omponents. |
+---------+---------+----------+------------+------------+------------+
| **Im    | O       | Costs    | ₱28        | Medium:    | Improves   |
| plement | ffloads | for CDN  | ,000--₱280 | Requires   | website    |
| a CDN   | traffic | s        | ,000/month | i          | speed and  |
| (       | from    | ervices. |            | ntegrating | reduces    |
| Content | origin  |          |            | the CDN    | load on    |
| D       | s       | Requires |            | with the   | servers by |
| elivery | ervers. | int      |            | website    | caching    |
| Net     |         | egration |            | and        | content    |
| work)** | Reduces | and      |            | c          | closer to  |
|         | l       | config   |            | onfiguring | users.     |
|         | atency. | uration. |            | caching    |            |
|         |         |          |            | rules.     |            |
+---------+---------+----------+------------+------------+------------+
| **In    | P       | Does not | ₱56        | Medium:    | Protects   |
| troduce | rotects | address  | ,000--₱168 | Involves   | system     |
| WAF     | against | per      | ,000/month | setting up | integrity, |
| (Web    | DDoS    | formance |            | the WAF,   | ensuring   |
| Appl    | and     | issues.  |            | defining   | legitimate |
| ication | other   |          |            | security   | traffic    |
| Fire    | t       | Requires |            | rules, and | flows      |
| wall)** | hreats. | mo       |            | ongoing    | smoothly   |
|         |         | nitoring |            | ma         | while      |
|         | E       | and      |            | intenance. | blocking   |
|         | nhances | updates. |            |            | malicious  |
|         | se      |          |            |            | request    |
|         | curity. |          |            |            |            |
+---------+---------+----------+------------+------------+------------+

**Grading Rubric:**

  -------------------------------------------------------------------------------
  Criteria           Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                            4pts
  ------------------ ------------------ ------------------- ---------------------
  **Problem          Accurately         Identifies the main Identifies a problem
  Identification**   identifies the     problem and         but lacks clarity or
                     primary problem    provides a basic    accuracy.
                     and provides a     explanation.        
                     detailed                               
                     explanation.                           

  **Solution         Proposes multiple  Proposes one or two Proposes a solution
  Proposal**         relevant solutions relevant solutions  but lacks feasibility
                     and provides       but lacks detailed  or relevance.
                     detailed           explanation.        
                     explanations,                          
                     including                              
                     potential                              
                     drawbacks and                          
                     benefits.                              

  **Evaluation of    Provides a         Provides a basic    Does not evaluate the
  Solutions**        thorough           evaluation of the   proposed solutions or
                     evaluation of the  proposed solutions, provides a
                     proposed           but lacks depth.    superficial
                     solutions,                             evaluation.
                     considering                            
                     factors like cost,                     
                     complexity, and                        
                     potential impact.                      

  Score:                                                    /30
  -------------------------------------------------------------------------------

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![](vertopal_9cd268d27e3f47da9dc851aec016c912/media/image3.webp){width="4.666666666666667in"
height="3.740972222222222in"}

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

**\
**![](vertopal_9cd268d27e3f47da9dc851aec016c912/media/image4.png){width="5.166666666666667in"
height="6.570138888888889in"}

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

> The proposed design includes the addition of two ISPs to ensure
> greater reliability and redundancy for internet connectivity. This
> dual-ISP setup lessens the risk of a single point of failure,
> providing continuous internet access even if one ISP encounters
> issues. Redundancy is also implemented across all critical devices,
> including two core switches and two edge routers. This redundant
> design ensures high availability and fault tolerance which prevents
> network downtime in case of device failure. By incorporating these
> redundant elements, the network is made more robust, maintaining
> service continuity and improving overall network reliability.

  ------------------------------------------------------------------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts
  ----------------- ------------------ ------------------- ---------------------
  **Network         Accurately         Identifies key      Identifies some basic
  Analysis**        identifies         network components  network components
                    potential          and some potential  but lacks a
                    bottlenecks,       bottlenecks.        comprehensive
                    security risks,                        analysis.
                    and capacity                           
                    limitations.                           

  **Scalability     Proposes multiple  Proposes some       Proposes limited
  Planning**        relevant solutions relevant            scalability
                    and provides       scalability         strategies.
                    detailed           strategies but      
                    explanations,      lacks detail.       
                    including                              
                    potential                              
                    drawbacks and                          
                    benefits.                              

  **Evaluation of   Proposes           Provides a basic    Does not evaluate the
  Solutions**       comprehensive      evaluation of the   proposed solutions or
                    scalability        proposed solutions, provides a
                    strategies,        but lacks depth.    superficial
                    including specific                     evaluation.
                    recommendations                        
                    for hardware                           
                    upgrades, software                     
                    configurations,                        
                    and network                            
                    optimizations.                         

  **Proposed        Provides a         Provides a basic    Does not provide a
  Design**          detailed and       design but lacks    clear and detailed
                    well-justified     specific details    design.
                    design, including  and justifications. 
                    network diagrams,                      
                    configuration                          
                    details, and                           
                    implementation                         
                    plans.                                 

  **Evaluation and  Provides a         Provides a basic    Does not evaluate the
  Justification**   thorough           evaluation of the   proposed solutions or
                    evaluation of the  proposed solutions, provides a
                    proposed           but lacks depth.    superficial
                    solutions,                             evaluation
                    considering                            
                    factors like cost,                     
                    complexity, and                        
                    potential impact.                      

  Score:                                                   /50
  ------------------------------------------------------------------------------
