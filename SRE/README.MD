#### Here are Some Resources: 

1. [Site Reliability Engineer (SRE) Interview Preparation Guide](https://github.com/mxssl/sre-interview-prep-guide)
2. [InterviewBit - SRE Interview Questions](https://www.interviewbit.com/sre-interview-questions/)
3. [NovelVista - Top 22 Site Reliability Engineer Interview](https://www.novelvista.com/blogs/devops/top-22-sre-interview-question-answer-2020)
4. [Indeed - 34 Site Reliability Engineer Interview Questions](https://www.indeed.com/career-advice/interviewing/site-reliability-engineer-interview)
5. [Gremlin - SRE Interview Questions](https://www.gremlin.com/site-reliability-engineering/sre-interview-questions-and-job-descriptions/)
6. [Mindmajix - SRE Interview Questions](https://mindmajix.com/sre-interview-questions)
7. [DevOpsSchool- Top 20 SRE interview questions and answers.](https://www.devopsschool.com/blog/top-20-sre-interview-questions-and-answers/)
8. [Coding-Ninjas - SRE Interview Questions](https://www.codingninjas.com/studio/library/sre-interview-questions)

**NOTE** - Above resources are not mine and belong to their owners, questions may overlap.

## Table of Contents

- [Questions](#questions)
- [Some Scenario-based SRE question](#some-scenario-based-sre-question)

## Essentials

Site Reliability Engineering (SRE) and DevOps are related but distinct disciplines, and their interview processes can differ based on the specific roles and responsibilities involved. Here are some key differences in how a SRE interview might differ from a DevOps interview:

1. Focus on Responsibilities:
   - SRE interviews often focus on reliability, scalability, and availability of systems. Questions may revolve around designing and implementing monitoring, incident response, and service level objectives (SLOs).
   - DevOps interviews may emphasize collaboration between development and operations teams, automation, and the entire software delivery lifecycle, including CI/CD pipelines and infrastructure as code (IaC).

2. Technical Expertise:
   - SRE interviews may assess skills related to distributed systems, performance optimization, and deep

 system knowledge, as SREs need to ensure services are highly available.
   - DevOps interviews may concentrate more on automation tools, scripting, and knowledge of various DevOps practices like continuous integration, continuous deployment, and containerization.

3. Incident Management:
   - SRE interviews often include questions about incident management, including how candidates handle on-call responsibilities, incident response, post-mortem analysis, and reliability improvement.
   - DevOps interviews may touch on incident response as well, but they might not delve as deeply into post-incident processes compared to SRE interviews.

4. Tools and Technologies:
   - SRE roles might require a deep understanding of specific technologies like Kubernetes, Prometheus, Grafana, and reliability engineering frameworks.
   - DevOps roles may involve a broader range of tools, including CI/CD tools (e.g., Jenkins, GitLab CI), configuration management tools (e.g., Ansible, Chef), and cloud platforms.

5. Collaboration and Soft Skills:
   - Both SREs and DevOps professionals need good communication and collaboration skills, but SREs may place more emphasis on coordinating with development teams to meet reliability goals.
   - DevOps roles often stress collaboration between development and operations teams to streamline software delivery.

Ultimately, the specific interview process can vary widely depending on the company, the job description, and the organization's approach to SRE and DevOps. Candidates should carefully review the job posting and prepare accordingly, focusing on the aspects that align with the role's requirements.


# Questions


1. **What is the difference between uptime and availability?**
   - **Answer:** Uptime is the total time a system is operational, while availability measures the percentage of time a system is accessible and functioning. Availability takes into account planned maintenance and unplanned downtime.

2. **Explain the concept of Service Level Objectives (SLOs) and Service Level Indicators (SLIs).**
   - **Answer:** SLOs are specific reliability targets that define acceptable levels of performance. SLIs are the metrics used to measure system performance, like latency or error rates. SLOs are derived from SLIs and are used to ensure the desired level of reliability.

3. **What is the purpose of an Error Budget in SRE?**
   - **Answer:** An Error Budget represents the allowable amount of downtime or errors that a service can have while still meeting its SLO. It helps teams strike a balance between rapid development and maintaining reliability.

4. **How do you approach designing a highly available system architecture?**
   - **Answer:** Start with redundancy, distribute components across multiple availability zones or regions, employ load balancing, implement failover mechanisms, use monitoring and alerting to detect issues proactively, and regularly perform disaster recovery drills.

5. **Explain the concept of "Toil" in SRE.**
   - **Answer:** Toil refers to repetitive, manual operational work that is devoid of long-term value and should be automated or eliminated. SREs aim to reduce toil to free up time for more strategic tasks.

6. **What is the difference between a Service Level Agreement (SLA) and an SLO?**
   - **Answer:** An SLA is a formal contract with customers that defines service expectations and penalties for non-compliance. An SLO is an internal target used to measure and manage service reliability. SLOs are often more aggressive than SLAs.

7. **How would you handle a critical incident in a production environment?**
   - **Answer:** I would follow an incident response plan, including immediate detection, alerting, and communication with the team. Then, I would prioritize mitigating the issue, conduct a post-mortem analysis to identify the root cause, and implement preventive measures.

8. **Explain the importance of monitoring and alerting in SRE.**
   - **Answer:** Monitoring provides visibility into system performance, while alerting notifies teams of issues. Both are crucial for detecting anomalies, diagnosing problems, and maintaining service reliability.

9. **Can you describe a scenario where you implemented automation to improve system reliability?**
   - **Answer:** I automated routine tasks like log rotation and backups, reducing manual errors and saving time. Additionally, I automated scaling to handle traffic spikes, ensuring our services remained responsive under load.

10. **What is Chaos Engineering, and how does it contribute to system reliability?**
    - **Answer:** Chaos Engineering involves intentionally injecting failures or stress into a system to discover vulnerabilities and weaknesses. By doing so, teams can proactively identify issues and make the system more resilient to failures.

11. **What is the purpose of a Service Level Indicator (SLI)?**
    - **Answer:** SLIs are specific measurements used to quantify the behavior of a service. They serve as the basis for defining SLOs and help teams assess whether their service is meeting reliability targets.

12. **How would you define a "golden signal" in monitoring?**
    - **Answer:** A golden signal refers to the most critical metric or indicator for a particular service, typically associated with user experience. Common golden signals include latency, error rate, and traffic.

13. **Explain the concept of a "blameless post-mortem."**
    - **Answer:** A blameless post-mortem is a structured process for analyzing incidents or outages without assigning blame to individuals. Its goal is to identify systemic issues, learn from failures, and improve reliability, culture, and processes.

14. **What is the difference between proactive and reactive SRE work?**
    - **Answer:** Proactive work involves measures taken to prevent incidents and improve system reliability, such as automation and capacity planning. Reactive work deals with responding to incidents and minimizing their impact.

15. **Describe the principles of the "Three Rs" in incident response.**
    - **Answer:** The Three Rs are Recognize (detecting an incident), Respond (taking immediate action to mitigate it), and Resolve (addressing the underlying issue and preventing future occurrences). These principles guide effective incident management.

16. **How do you approach capacity planning for a service to ensure it meets performance and reliability requirements?**
    - **Answer:** Capacity planning involves monitoring resource utilization, forecasting future demand, and ensuring that the system has enough resources to handle traffic spikes and growth while meeting performance and reliability goals.

17. **Can you explain the concept of "Error Budget Burn" and how it relates to SLOs?**
    - **Answer:** Error Budget Burn measures how much of the allowable error budget has been consumed over a specific period. When the error budget is exhausted, it signals that the service is not meeting its reliability goals, and teams may need to slow down feature development to focus on stability.

18. **What is the role of chaos testing in SRE, and can you provide an example of a chaos experiment?**
    - **Answer:** Chaos testing involves intentionally introducing disruptions or failures into a system to evaluate its resilience. An example experiment might involve randomly terminating instances in a cluster to assess if the system can maintain availability.

19. **How do you prioritize reliability work alongside feature development in a fast-paced software development environment?**
    - **Answer:** Prioritizing reliability work involves assessing the impact on user experience and the business. Critical reliability issues and SLO violations should take precedence, but a balance must be struck to avoid stalling feature development.

20. **What are some key skills or qualities that make a successful SRE?**
    - **Answer:** Successful SREs typically possess strong problem-solving skills, a deep understanding of distributed systems, expertise in automation and scripting, effective communication, and a commitment to a culture of reliability and collaboration.

21. **What is the purpose of an Error Budget Policy, and how does it impact decision-making in SRE?**
    - **Answer:** An Error Budget Policy defines how much unreliability or downtime is acceptable within a specific timeframe. It guides decisions by helping teams balance innovation and reliability. If the error budget is exhausted, it may trigger a slowdown in feature development to focus on stability.

22. **Can you explain the concept of "Toil Ratio"?**
    - **Answer:** The Toil Ratio is the proportion of time spent on manual, repetitive operational tasks (toil) compared to time spent on engineering work to eliminate or automate that toil. A lower Toil Ratio indicates a more efficient and reliable system.

23. **What is Observability, and how does it differ from Monitoring?**
    - **Answer:** Observability is the capacity to understand the internal state of a system through its external outputs, like logs, metrics, and traces. Monitoring focuses on collecting and visualizing these data points, while observability emphasizes the ability to explore and troubleshoot complex systems.

24. **Explain the concept of "Error Budgets as a Feature."**
    - **Answer:** Error Budgets as a Feature is an approach where a service team can choose to allocate a portion of its error budget to implement new features or experiments. This allows teams to make informed trade-offs between reliability and innovation.

25. **What is the role of Change Management in SRE, and how does it relate to risk mitigation?**
    - **Answer:** Change Management involves processes for reviewing, approving, and implementing changes to a system. It helps mitigate risks by ensuring that changes are well-tested, monitored, and that rollbacks are possible in case of issues, reducing the likelihood of outages.

26. **How do you handle a situation where SLOs are consistently not met?**
    - **Answer:** When SLOs are not consistently met, it's crucial to conduct a detailed analysis of the root causes. This may involve improving monitoring, automation, or revisiting the SLOs themselves to ensure they align with user expectations. The goal is to continuously improve reliability.

27. **Explain the role of Chaos Monkey in SRE practices.**
    - **Answer:** Chaos Monkey is a tool developed by Netflix that simulates random failures in a distributed system. Its purpose is to test the system's resilience by deliberately causing failures in a controlled environment. It helps identify weaknesses and encourages redundancy and fault tolerance.

28. **How do you ensure security considerations are integrated into SRE practices?**
    - **Answer:** Security should be a fundamental aspect of SRE. It involves proactive threat modeling, regular security assessments, and ensuring that security controls are part of the automation and infrastructure as code processes to prevent vulnerabilities.

29. **Describe a scenario where you successfully reduced the Mean Time to Detect (MTTD) or Mean Time to Recover (MTTR) for an incident.**
    - **Answer:** Provide an example of how you improved monitoring, alerting, or incident response processes to detect issues faster or recover more quickly. Highlight the impact on system reliability.

30. **What are some best practices for conducting a blameless post-mortem analysis?**
    - **Answer:** Some best practices include involving all stakeholders, focusing on systemic issues rather than individual blame, documenting the incident timeline and contributing factors, and creating actionable recommendations for improvement.

31. **What is "on call" in SRE**

    - **Answer:** In Site Reliability Engineering (SRE), being "on call" refers to a practice where SREs (Site Reliability Engineers) or other operational personnel take turns being responsible for responding to incidents and ensuring the reliability of services outside of regular working hours, including evenings, weekends, and holidays. This practice is often referred to as being part of an "on-call rotation."

    Here are key aspects of being "on call" in SRE:

    1. **Incident Response:** When an SRE is on call, they are the first responders to incidents or service disruptions that may occur outside of business hours. Their primary responsibility is to investigate, diagnose, and resolve these incidents promptly to minimize service downtime and user impact.

    2. **Availability:** SREs must be reachable and available at all times during their on-call shift. This typically involves carrying a mobile device, being responsive to alerts and notifications, and being ready to log in and take action when needed.

    3. **Rotation:** On-call responsibilities are typically organized into rotations, where each SRE takes a turn being on call for a specific period, such as a week or a few days. After their shift, they pass the on-call duties to the next team member in the rotation.

    4. **Escalation:** In the event of a particularly severe incident or if an SRE needs additional support, there is often an escalation process in place. This may involve contacting more senior SREs or engaging other relevant teams within the organization.

    5. **Documentation:** SREs maintain documentation and runbooks to guide incident response procedures. This documentation helps ensure consistency in handling incidents and allows other team members to assist if necessary.

    6. **Post-Incident Analysis:** After an incident is resolved, SREs often conduct post-mortem or post-incident analysis to understand the root cause, document lessons learned, and implement improvements to prevent similar incidents in the future.

    Being on call is a critical aspect of SRE because it ensures that services remain reliable and available to users 24/7. It also aligns with the SRE principle of shared responsibility, where engineers who build and operate services share the responsibility for their reliability, including responding to incidents and addressing reliability issues promptly.


# Some Scenario-based SRE question

1. We have a web application that works in a simple client server model. There are two parts to the web app. The frontend single page application that is hosted using s3 and is distributed using a CDN. The second part is the api backend that is hosted on, lets say ec2 instances and uses a database and a cache. Can you elaborate on how the networking should be set up for the backend api server? Note: The backend api server needs to interact with external third party vendors.

In this application, let's say that there is a high throughput requirement, let's say registrations which are write heavy activity, what changes would you make to the infra so that the backend api server can handle this increased write throughput.  

We are going to go over a couple of scenarios where the above web application server is not working as expected, and I will like you to troubleshoot it to find the root cause of the issue and figure out the way to get the server to resume normal operation.

The server is able to handle around 10 requests per second in normal working condition.

Request logs of the web application server in normal working condition:

```bash

[1722306573] - 200 - GET - /organization/12345/users/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.158.1.38
[1722306573] - 204 - POST - /valid_path_1/12345/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.88
[1722306576]  - 200 - GET - /valid_path_2/ - Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/51.0.2704.106 Safari/537.36 OPR/38.0.2220.41
[1722306586] - 200 - GET - /valid_path_4/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.88
```

Scenario 1:

The application is not working as expected with users getting a loader for a short duration of time after which an error message displays with a message like: "Failed to get response from the backend. Please refresh and try again!". 

```bash
[1722306573] - 404 - GET - /index.php - NodeJS - 192.158.1.38

[1722306573] - 404 - POST - /private_files - NodeJS - 192.158.1.38

[1722306576] - 404 - GET - /?debug_mode=true - NodeJS - 192.158.1.38

[1722306586] - 200 - GET - /valid_path_2/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.88

[1722306586] - 404 - GET - /logs.txt - NodeJS - 192.158.1.38

[1722306586] - 404 - GET - /?admin_mode=true - NodeJS - 192.158.1.38

[1722307086] - 503 - GET - /valid_path_2/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.88

[1722307106] - 503 - GET - /valid_path_3/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.80

[1722307586] - 502 - GET - /valid_path_4 - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.84

[1722307986] - 502 - GET - /valid_path_5/ - Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0 - 192.156.1.31
```

CPU utilization of the server is close to 99%, Memory utilization is under 75%. Average Request TPS is 53 over a 5 minute period. DB cpu utilization is less than 40% and memory utilization is less than 30%.

**Answer:** Let’s go through everything in detail, starting with the architecture and networking setup, then scaling strategies, and finally dive into the incident and root cause analysis.

---

### ✅ Backend API Server Networking Setup

#### **Basic Requirements**
Your backend API server (hosted on EC2) needs to:
- Serve requests from the frontend (S3 + CDN)
- Communicate with a database and cache (likely within the same VPC)
- Access external third-party APIs (like payment gateways, SMS/email vendors)
- Be secure from unauthorized access

#### **Ideal Networking Design**

1. **VPC Setup**
   - **VPC**: Define a Virtual Private Cloud to isolate resources.
   - **Subnets**:
     - **Private subnets**: Place EC2 instances, DB, and cache here. Not directly internet-accessible.
     - **Public subnet**: For NAT Gateway and Bastion host (if needed).

2. **Security Groups**
   - EC2 SG:
     - Allow HTTP(S) from the CDN IP range or ALB.
     - Allow outbound to the internet (for external APIs).
   - DB SG:
     - Only allow traffic from EC2 SG.
   - Cache SG:
     - Allow only EC2 SG access.

3. **Internet Access**
   - **NAT Gateway** in a public subnet allows EC2 in private subnets to access the internet (for third-party API calls).
   - **No public IPs** on EC2s.

4. **Load Balancer (ALB/NLB)**
   - Expose the API via an Application Load Balancer.
   - Terminate HTTPS at the ALB.
   - Route requests to EC2 instances.

5. **DNS**
   - Use Route 53 or other DNS services to route `api.example.com` to the ALB.

---

### 📈 High Throughput: Write-Heavy Scaling Strategy

#### Key Concerns
- Increased concurrent POST/PUT requests (e.g., registrations).
- Write spikes to database and cache.

#### Scaling Approaches

1. **Auto Scaling**
   - Use CPU/memory/TPS as scaling metrics.
   - Add more EC2s in the group behind the ALB.

2. **Horizontal DB Write Scaling**
   - **Primary-replica DB setup** for read/write split.
   - Use **write buffering**, **queueing**, or **batching** if consistent latency is tolerable.
   - **Write sharding** (if you expect huge scale).

3. **Asynchronous Processing**
   - Push registration writes to a queue (e.g., SQS/Kafka).
   - Worker processes consume and write to DB.

4. **Caching**
   - Cache duplicate registration checks, metadata, etc., using Redis/Memcached.

5. **Connection Pooling**
   - Ensure API servers use DB connection pools to avoid exhaustion.

6. **Use Faster Storage**
   - Use GP3 or provisioned IOPS volumes for DB if write latency is an issue.

7. **Rate Limiting / Throttling**
   - Prevent abuse or DDoS under high write load.

---

### 🚨 Troubleshooting Scenario 1: Backend Unavailable

#### Observations

- Increase in **404**, **502**, **503** errors.
- Some paths are valid and return 200, while others fail.
- CPU utilization at **99%**, memory is OK.
- TPS has increased significantly (from 10 → 53).
- DB is not a bottleneck.

#### Log Insights

- Requests like `/index.php`, `/?admin_mode=true`, and `/logs.txt` are **not valid paths**. Suggests bot or scanner traffic.
- Spikes in 502/503: Application is **overwhelmed** or **crashing**.
- Some 404s with strange user agents (`NodeJS`) → possibly automated/bot traffic.

---

#### Likely Root Cause

**Application overload due to bot traffic / path scanning attacks**  
This bot traffic is sending invalid requests, possibly triggering expensive error handling logic, leading to CPU saturation.

---

#### Resolution Plan

1. **Immediate**
   - Block suspicious IPs or User Agents using WAF (AWS WAF, Cloud Armor, etc.).
   - Serve 403 immediately for known bad patterns (e.g., `.php`, `debug_mode`, `admin_mode`).
   - Add rate-limiting or CAPTCHA at frontend for sensitive actions.

2. **Mid-Term Fix**
   - Add caching for static/dynamic content wherever possible.
   - Use AWS Shield or Cloudflare for DDoS protection.
   - Optimize API code to fail fast on invalid routes.
   - Use a reverse proxy (e.g., NGINX) to filter invalid paths.

3. **Monitoring**
   - Set up alerts for CPU > 80%, sudden surge in 4xx or 5xx.
   - Log and aggregate User Agents/IPs to detect bots early.

4. **Infra Scaling**
   - Enable auto-scaling based on CPU load.
   - Use a queue-based architecture to decouple expensive operations.
  