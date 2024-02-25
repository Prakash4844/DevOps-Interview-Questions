#### Here are Some Resources: 

1. [InterviewBit - GCP Interview Questions](https://www.interviewbit.com/gcp-interview-questions/)
2. [intellipaat - Top 30 GCP Interview Questions](https://intellipaat.com/blog/interview-question/google-cloud-platform-interview-questions/)
3. [K21Academy - 30 GCP Interview Questions and Answers](https://k21academy.com/google-cloud/top-30-gcp-interview-questions-and-answers/)
4. [TestGorilla - GCP Interview Questions](https://www.testgorilla.com/blog/gcp-interview-questions/)
5. [Mindmajix - GCP Interview Questions](https://mindmajix.com/google-cloud-interview-questions)
6. [Turning - GCP Interview Questions and Answers](https://www.turing.com/interview-questions/gcp)
7. [Flexiple - Top 18 GCP Interview Questions and Answers](https://flexiple.com/gcp/interview-questions)
8. [WhizLabs - Top 40+ GCP Interview Questions](https://www.whizlabs.com/blog/google-cloud-interview-questions/)
9. [NWKings - Top Most-Asked GCP Interview Questions and Answers](https://www.nwkings.com/gcp-interview-questions-and-answers)


**NOTE** - Above resources are not mine and belong to their owners, questions may overlap.

## Table of Contents

1. [General Questions](#questions)
2. [Scenario-based Questions](#some-scenario-based-devops-question)

# Questions

## Essentials

**1. What is GCP?**

Google Cloud Platform (GCP) is a suite of cloud computing services offered by Google. GCP provides a wide range of cloud-based infrastructure and platform services that businesses and developers can use to build, deploy, and scale applications and services. These services encompass computing, storage, databases, machine learning, data analytics, networking, and more. Some key aspects of GCP include:

1. **Compute Services**: GCP offers a variety of virtual machines (VMs) and container services, including Google Compute Engine, Google Kubernetes Engine (GKE), and App Engine, for running applications.

2. **Storage Services**: GCP provides scalable and durable storage solutions, such as Google Cloud Storage, Cloud SQL, and Bigtable, as well as managed file storage with Google Cloud Filestore.

3. **Databases**: GCP offers managed database services like Google Cloud SQL, Cloud Bigtable, and Cloud Spanner, supporting SQL and NoSQL databases.

4. **Machine Learning and AI**: GCP includes machine learning and artificial intelligence services like Google AI Platform, Vision AI, Natural Language AI, and AutoML, allowing users to build and deploy AI models.

5. **Data Analytics**: Services like BigQuery and Dataflow enable real-time data processing, data warehousing, and analytics.

6. **Networking**: GCP provides robust networking capabilities with services like Virtual Private Cloud (VPC), Load Balancers, and Cloud Interconnect for connecting to your on-premises data centers.

7. **Security and Identity**: Google Cloud IAM (Identity and Access Management) allows fine-grained control over access to resources, and GCP provides tools for securing data and applications.

8. **Developer Tools**: GCP offers various tools and APIs for development, including Google Cloud SDK, Cloud Source Repositories, and Cloud Build.

9. **Hybrid and Multi-Cloud**: GCP provides solutions for hybrid and multi-cloud deployments, allowing you to connect on-premises environments with GCP and even run workloads on other cloud platforms.

10. **IoT and Edge Computing**: GCP includes services for Internet of Things (IoT) and edge computing, such as Cloud IoT Core and Edge TPU for AI at the edge.

11. **Management and Monitoring**: Google Cloud provides tools like Google Cloud Console and Stackdriver for monitoring and managing GCP resources.

GCP is known for its global network infrastructure, data centers, and the use of Google's expertise in machine learning and data analytics. It's used by a wide range of organizations, from startups to enterprises, for cloud-based solutions, data storage, and application deployment.

### GCP Hierarchy

**2. How is GCP organised hierarchically?**

Google Cloud Platform (GCP) is organized hierarchically as follows:

1. **Organizations**: At the top level, there are organizations, which are typically represented by your company or institution. An organization can have multiple projects within it.

2. **Projects**: Projects are used to organize and manage resources within GCP. Each project is isolated and contains its own set of resources, billing, and permissions. Projects can represent different applications or departments within an organization.

3. **Resources**: Within each project, you have various resources like virtual machines (VMs), storage buckets, databases, and more. These resources are where you deploy and manage your applications and services.

4. **Folders** (Optional): Some organizations may use folders to further structure their projects. Folders allow you to group projects together for easier management, especially in large organizations with many projects.

5. **Billing**: Billing is associated with each project. It allows you to track and manage the costs incurred by the resources used within that project.

6. **Permissions**: GCP uses Identity and Access Management (IAM) to control access to resources. You can grant permissions at the organization, project, folder, or resource level.

This hierarchical structure provides flexibility and control, allowing organizations to manage their resources and access control efficiently. It's important to plan your GCP hierarchy carefully to align with your organization's needs.

**3. How does GCP Hierarchy compares to Microsoft Azure's Hierarchy?**

Google Cloud Platform (GCP) and Microsoft Azure have similar hierarchical structures in some aspects, but there are also differences.

**Google Cloud Platform (GCP) Hierarchy:**
1. **Organizations**: The highest level, representing your company or institution.
2. **Projects**: Used to organize and manage resources within GCP.
3. **Resources**: Within projects, you have various cloud resources.

**Microsoft Azure Hierarchy:**
1. **Management Groups**: At the top level, these are used to organize subscriptions and enforce policies across multiple Azure subscriptions.
2. **Subscriptions**: Similar to GCP projects, these contain Azure resources and are associated with billing.
3. **Resource Groups**: Within subscriptions, you create resource groups to organize and manage related Azure resources.
4. **Resources**: Similar to GCP, these are the actual cloud services and virtual resources like VMs, databases, etc.

**Key Differences:**
1. **Management Groups**: Azure has an additional layer called "Management Groups" that allows you to organize subscriptions and apply policies at a higher level than individual subscriptions. GCP doesn't have an equivalent to this.

2. **Resource Groups**: While Azure uses resource groups to organize resources within subscriptions, GCP organizes resources directly within projects. Azure's resource groups provide more granular resource-level organization.

3. **Hierarchical Policy Enforcement**: Azure's hierarchy allows for hierarchical policy enforcement through Management Groups, which can be useful for governance and compliance. GCP's IAM is more project-focused.

4. **Billing**: Both platforms associate billing with the hierarchy, but Azure also offers more flexibility in cost management through features like cost centers and budgets.

5. **Identity and Access Management (IAM)**: Both platforms use IAM for access control, but Azure's IAM is more subscription-centric, while GCP's is more project-centric.

It's important to note that while there are differences in the hierarchy, both GCP and Azure provide the tools and flexibility needed to manage cloud resources effectively. The choice between them often depends on your organization's specific requirements and preferences.

**4. How does GCP hierarchy compare to Azure's? As azure contain more levels, Azure AD, management group to 6 levels, Subscription, Resource group and resource. It seems azure is more flexible?**

Azure's hierarchy does indeed provide more levels of organization and flexibility compared to GCP. Azure's hierarchy includes Management Groups, Subscriptions, Resource Groups, and Resources, which can be structured in a more granular way.

Azure's flexibility in this regard allows for more fine-grained control over resource organization, policy enforcement, and cost management. The presence of Azure Active Directory (Azure AD) also adds another layer for identity and access management, further enhancing its organizational capabilities.

While GCP's hierarchy with Organizations, Projects, and Resources is suitable for many use cases, Azure's additional layers like Management Groups and Resource Groups offer a higher degree of control and organization, especially in larger and more complex environments.

Ultimately, the choice between GCP and Azure should consider the specific needs of your organization and the level of hierarchy and control you require. Azure's flexibility can be advantageous in scenarios where a more intricate organizational structure is necessary.

### GCP IAM

**5. What do you know about GCP IAM**

Google Cloud Identity and Access Management (IAM) is a crucial component of Google Cloud Platform (GCP) that manages access control and permissions for cloud resources. Here's an overview of GCP IAM:

1. **Identity Management**: GCP IAM helps you manage who (identities) has access to what resources within your GCP environment. Identities can be individual users, groups of users, or service accounts.

2. **Resource Hierarchy**: IAM is hierarchical and aligned with GCP's project-based resource hierarchy. You can set permissions at various levels, such as the organization, folder, project, or resource level.

3. **Roles**: IAM uses predefined roles that define a set of permissions. These roles can be assigned to users, groups, or service accounts. Examples of roles include Viewer, Editor, and Owner, but GCP offers a wide range of roles, and you can also create custom roles to suit your specific needs.

4. **Least Privilege Principle**: It's a best practice to follow the principle of least privilege. This means granting only the necessary permissions for users or service accounts to perform their tasks, reducing the risk of accidental or unauthorized actions.

5. **Conditional Role Binding**: IAM supports conditional role bindings, allowing you to set conditions for when permissions are granted. For example, you can restrict access to specific IP ranges or require multi-factor authentication (MFA) for certain actions.

6. **Audit Logging**: GCP IAM provides audit logging capabilities, allowing you to monitor and track access and changes to permissions and resources. This helps in compliance and security auditing.

7. **Service Accounts**: Service accounts are special identities used by applications or services running on GCP. IAM allows you to grant permissions to service accounts, making it possible for applications to access GCP resources securely.

8. **Granular Control**: IAM offers granular control over permissions, including the ability to specify permissions for specific resources or resource types. This flexibility allows you to tailor access control to your specific use cases.

9. **Integration with Other GCP Services**: IAM integrates seamlessly with other GCP services, such as Cloud Storage, BigQuery, and Compute Engine, allowing you to manage access to these resources effectively.

10. **Security and Compliance**: Properly configuring IAM is essential for ensuring the security and compliance of your GCP environment. It helps you maintain control over your cloud resources and data.

Overall, GCP IAM plays a critical role in securing and managing your GCP resources by providing fine-grained access control and permissions management. It's a fundamental aspect of cloud security and governance.

**6. What is principal in GCP IAM?**

In Google Cloud Identity and Access Management (IAM), a "principal" refers to an entity that can request access to resources or perform actions within your Google Cloud Platform (GCP) environment. Principals can represent users, service accounts, or Google Groups. Here's a breakdown of these principal types:

1. **User**: A user principal typically represents an individual who interacts with GCP resources. Users can be your organization's employees, contractors, or anyone with a Google Account granted access to your GCP project or organization.

2. **Service Account**: A service account is a special type of principal used by applications, virtual machines, and services running on GCP. Service accounts are used to authenticate and access GCP resources securely. They are often used for automation and integration purposes.

3. **Google Group**: A Google Group is a collection of Google Accounts. You can assign permissions to an entire group, making it easier to manage access for multiple users simultaneously. When you grant permissions to a Google Group, all members of the group inherit those permissions.

Principals are essential for access control in GCP IAM. You can grant roles and permissions to these principals at various levels in your GCP resource hierarchy (organization, folder, project, or resource). By assigning roles to principals, you define what actions they are allowed or denied for specific resources or services.

For example, you can grant the "Storage Object Viewer" role to a user principal, allowing them to view objects in a Cloud Storage bucket. Or, you can assign a service account the "Compute Engine Instance Admin" role to manage virtual machine instances.

Overall, principals in GCP IAM are the entities to which you delegate access rights and permissions, enabling fine-grained control over who can perform actions on your GCP resources.

**7. What are roles in GCP IAM?**

In Google Cloud Identity and Access Management (IAM), roles define a set of permissions that determine what actions can be performed on GCP resources. Roles are a fundamental part of access control in GCP, and they help you grant appropriate levels of access to users, service accounts, and groups. Here's an overview of roles in GCP IAM:

1. **Predefined Roles**: GCP provides a set of predefined roles that cover common use cases. These roles are ready to use and include permissions tailored for specific job functions. Examples of predefined roles include "Viewer," "Editor," and "Owner." Each predefined role has a specific set of permissions associated with it.

2. **Custom Roles**: While predefined roles cover many scenarios, you can create custom roles to meet specific requirements. Custom roles allow you to define a granular set of permissions by selecting individual permissions or combining them from different services. This flexibility enables you to tailor access control precisely to your needs.

3. **Primitive Roles** (Legacy): Primitive roles are legacy roles that provide a basic level of access control. They include roles like "Project Viewer," "Project Editor," and "Project Owner." Google recommends using predefined or custom roles instead of primitive roles for more fine-grained control.

4. **Resource-Level Roles**: Some roles are designed for specific GCP resources, such as "Storage Object Viewer" for Cloud Storage or "BigQuery Data Viewer" for BigQuery. These roles grant permissions related to a particular type of resource.

5. **Service Management Roles**: These roles are used for managing APIs and services within your GCP project. For example, the "Service Usage Admin" role allows users to enable or disable services in a project.

Roles can be assigned to individual users, service accounts, or Google Groups at various levels in your GCP resource hierarchy, such as the organization, folder, project, or resource level. When you assign a role to a principal (user, service account, or group), they inherit the associated permissions.

It's important to follow the principle of least privilege when assigning roles, granting only the necessary permissions for individuals or service accounts to perform their tasks. Properly managing roles and permissions is critical for security and access control in your GCP environment.

**8. On what level can custom role be assigned in GCP IAM?**

Custom roles in Google Cloud IAM can be assigned at several levels within the GCP resource hierarchy. You have the flexibility to apply custom roles at the following levels:

1. **Project Level**: You can assign a custom role directly to a specific GCP project. This allows you to define custom access controls for that particular project. Users or service accounts with the custom role will have those permissions only within that project.

2. **Organization Level**: At the highest level of the GCP resource hierarchy, you can assign custom roles at the organization level. This grants permissions across all projects, folders, and resources within the entire organization. It's a way to define organization-wide access control.

3. **Resource Level**: Depending on the nature of the custom role and the services it applies to, you may be able to assign it directly to specific resources. For example, a custom role related to a Cloud Storage bucket could be assigned at the bucket level.

The choice of where to assign a custom role depends on your specific access control requirements and how you've structured your GCP environment. It's important to consider the scope of the permissions and ensure that you apply custom roles in a way that aligns with your organization's security and access control policies.

Remember that custom roles should be designed thoughtfully to grant the least privilege necessary for users or service accounts to perform their tasks while maintaining security and compliance.

**Note: You cannot define custom roles at the folder level. If you need to use a custom role within a folder, define the custom role at the organization level. You can only grant a custom role within the project or organization in which you created it. You cannot grant custom roles on other projects or organizations, or on resources within other projects or organizations.**

**9. How can I audit and monitor IAM activity in GCP?**

GCP provides tools such as Cloud Audit Logs and Cloud Monitoring for auditing and monitoring IAM activity. Cloud Audit Logs record all administrative and data access activities in your GCP environment, while Cloud Monitoring allows you to create custom metrics and alerts based on IAM-related events.

### GCP Service accounts

**10. What is a service account in GCP?**

A service account in GCP is a special type of Google account that represents non-human users within the GCP ecosystem. Unlike user accounts, which typically represent individual humans accessing GCP resources, service accounts are used for programmatic access by applications, virtual machines, or other services running on behalf of users or the system itself. Service accounts are designed to authenticate and authorize access to GCP APIs and services securely.

**11. How do service accounts differ from user accounts in GCP?**

Service accounts and user accounts serve distinct purposes within GCP:
 - **User accounts**: These represent individual humans who interact with GCP resources through the Cloud Console, command-line tools, or APIs. User accounts have associated passwords or other forms of authentication for login purposes.
 - **Service accounts**: These represent applications, services, or resources within the GCP environment itself. They are used for programmatic access and do not have passwords associated with them. Instead, they use cryptographic keys or OAuth 2.0 credentials for authentication. Service accounts are typically used by applications running on virtual machines, containers, or other computing resources.

**12. What are the best practices for managing service accounts in GCP?**

Effective management of service accounts is crucial for maintaining the security and integrity of your GCP environment. Some best practices include:
 - **Limiting the number of service accounts**: Minimize the proliferation of service accounts to reduce complexity and improve manageability.
 - **Applying the principle of least privilege**: Grant each service account only the permissions necessary to perform its intended function, reducing the risk of unauthorized access or misuse.
 - **Rotating service account keys**: Regularly rotate service account keys and OAuth 2.0 credentials to mitigate the risk of key compromise or unauthorized access.
 - **Monitoring service account activity**: Use tools like Cloud Audit Logs and Cloud Monitoring to monitor service account usage and detect suspicious or anomalous behavior.
 - **Securing service account credentials**: Safeguard service account keys and credentials by restricting access to authorized personnel and ensuring they are not exposed in code repositories or configuration files.

**13. How are service accounts authenticated in GCP?**

Service accounts are authenticated in GCP using either cryptographic keys or OAuth 2.0 access tokens:
 - **Cryptographic keys**: Service account keys are JSON-formatted files that contain a private key and other metadata. Applications use these keys to authenticate themselves to GCP services by signing requests with the private key.
 - **OAuth 2.0 access tokens**: Applications can obtain short-lived OAuth 2.0 access tokens for service accounts through the OAuth 2.0 authentication flow. These tokens are used to authenticate requests to GCP APIs on behalf of the service account.

**14. What are the different types of service accounts in GCP?**

GCP offers two types of service accounts:
 - **User-managed service accounts**: These are created and managed by users within a GCP project. User-managed service accounts offer greater control and customization, allowing users to specify the roles and permissions associated with the service account.
 - **Google-managed service accounts**: These are automatically created and managed by Google for specific GCP services, such as Compute Engine instances or App Engine applications. Google-managed service accounts are tightly integrated with the associated GCP service and are primarily used for internal service-to-service communication.

**15. How can service accounts be used for authentication and authorization in GCP?**

Service accounts can be used for authentication and authorization in GCP by associating them with IAM roles:
 - **Authentication**: Service accounts authenticate themselves to GCP services using cryptographic keys or OAuth 2.0 access tokens.
 - **Authorization**: By assigning appropriate IAM roles to service accounts, you can control the actions they are allowed to perform within your GCP environment. IAM roles define a set of permissions that govern what actions a service account can take on GCP resources and services. By granting the least privilege necessary, you can reduce the risk of unauthorized access or misuse.

### GCP Cloud Identity

**16. What is Google Cloud Identity?**
   - Google Cloud Identity is an identity and access management service provided by Google Cloud. It enables organizations to manage user identities, access controls, and security policies across their Google Cloud services, G Suite applications, and other SaaS (Software as a Service) applications.

**17. What are the key features of Google Cloud Identity?**
   - Google Cloud Identity offers a range of features to help organizations manage user identities and access:
     - **Single Sign-On (SSO)**: Enables users to access multiple applications with a single set of credentials, improving user experience and security.
     - **Identity and Access Management (IAM)**: Allows organizations to define granular access controls and permissions for users, groups, and service accounts.
     - **Multi-Factor Authentication (MFA)**: Enhances security by requiring users to provide additional authentication factors beyond passwords, such as SMS codes or security keys.
     - **User Provisioning and Deprovisioning**: Streamlines user lifecycle management by automating the creation, modification, and removal of user accounts.
     - **Security Policies**: Enables organizations to enforce security policies, such as password complexity requirements and account lockout policies, to protect user accounts.
     - **Audit Logging and Reporting**: Provides visibility into user activity and access events through audit logs and reporting tools.

**18. How does Google Cloud Identity integrate with GCP?**
   - Google Cloud Identity seamlessly integrates with GCP to provide identity and access management capabilities for GCP resources and services. Organizations can use Google Cloud Identity to manage user identities, control access to GCP resources through IAM policies, and enforce security policies across their GCP environment.

**19. What are the benefits of using Google Cloud Identity with GCP?**
   - Integrating Google Cloud Identity with GCP offers several benefits:
     - **Centralized Identity Management**: Provides a single identity management solution for managing user identities and access controls across GCP services, G Suite applications, and other SaaS applications.
     - **Simplified User Access**: Enables users to access GCP resources and services with their existing Google accounts or corporate credentials, reducing the need for multiple sets of credentials.
     - **Enhanced Security**: Offers advanced security features such as multi-factor authentication (MFA) and security policies to protect user accounts and data in the GCP environment.
     - **Streamlined User Lifecycle Management**: Automates user provisioning and deprovisioning processes, ensuring that user accounts are created, modified, and removed in a timely manner.
     - **Compliance and Governance**: Helps organizations enforce compliance requirements and governance policies by providing audit logs, reporting tools, and access controls.

**20. What security measures are in place to protect Google Cloud Identity?**
   - Google Cloud Identity employs a range of security measures to protect user identities and data:
     - **Encryption**: User data is encrypted both in transit and at rest to protect it from unauthorized access.
     - **Multi-Factor Authentication (MFA)**: Users can enable MFA to add an extra layer of security beyond passwords, such as SMS codes or security keys.
     - **Security Controls**: Administrators can enforce security policies, such as password complexity requirements and account lockout policies, to protect user accounts.
     - **Audit Logging**: Google Cloud Identity logs user activity and access events to provide visibility into who accessed what resources and when.
     - **Continuous Monitoring**: Google monitors its systems for suspicious activity and responds to security incidents in real-time to mitigate potential threats.

**21. What are some best practices for using Google Cloud Identity?**
   - To maximize the security and effectiveness of Google Cloud Identity, organizations should consider implementing the following best practices:
     - **Enable Multi-Factor Authentication (MFA)**: Require users to enable MFA to add an extra layer of security to their accounts.
     - **Use IAM Roles and Permissions**: Define granular IAM roles and permissions to control access to GCP resources based on the principle of least privilege.
     - **Regularly Review Access Controls**: Periodically review and update IAM policies to ensure that users have the appropriate level of access to resources.
     - **Enforce Strong Password Policies**: Implement password complexity requirements and regular password expiration policies to strengthen account security.
     - **Monitor User Activity**: Monitor user activity and access events using audit logs and reporting tools to detect and respond to security incidents.
     - **Educate Users**: Provide security awareness training to educate users about best practices for protecting their accounts and data.

---

**22. What are various ways to interact with GCP?**

1. **Google Cloud Console (Web UI)**:
   - The Google Cloud Console is a web-based user interface provided by Google for managing GCP resources. It offers a graphical interface that allows users to interact with GCP services, configure settings, monitor resources, and access various management tools.
   - The Console provides a user-friendly environment suitable for tasks such as managing projects, creating virtual machines, configuring storage buckets, setting up databases, and monitoring performance metrics.
   - It is accessible via any modern web browser and does not require any additional software installation.

2. **Google Cloud SDK (Command-Line Interface)**:
   - The Google Cloud SDK is a set of command-line tools provided by Google for interacting with GCP services from the command line or terminal. It offers a powerful and flexible way to manage GCP resources, automate tasks, and integrate with other tools and scripts.
   - The Cloud SDK includes tools such as `gcloud`, `gsutil`, and `bq` (BigQuery) for performing various operations like managing resources, uploading/downloading files to/from Cloud Storage, and running queries on BigQuery datasets.
   - It provides a consistent command-line interface across different platforms (Windows, macOS, Linux) and can be easily scripted and automated using shell scripts or other programming languages.

3. **Google Cloud Client Libraries (Programming APIs)**:
   - Google Cloud Client Libraries are software development kits (SDKs) provided by Google in various programming languages, including Python, Java, Go, Node.js, and others. These libraries allow developers to programmatically interact with GCP services and resources from their applications.
   - Client libraries offer language-specific APIs for GCP services, making it easy to integrate GCP functionality into applications without dealing with low-level HTTP requests and authentication mechanisms.
   - Developers can use client libraries to perform tasks such as creating, reading, updating, and deleting resources, executing GCP API requests, handling authentication, and processing responses.

4. **Cloud Shell (Browser-Based Shell Environment)**:
   - Cloud Shell is a browser-based shell environment provided by Google Cloud Platform. It offers a command-line interface directly within the Google Cloud Console, allowing users to run commands and manage GCP resources without needing to install any software locally.
   - Cloud Shell provides access to the Google Cloud SDK, common Linux utilities, and a persistent 5 GB home directory stored in Cloud Storage.
   - It is ideal for performing quick tasks, running commands, testing scripts, and accessing GCP resources from any device with an internet connection and a web browser.

5. **Google Cloud APIs (RESTful APIs)**:
   - Google Cloud Platform offers a set of RESTful APIs that allow developers to programmatically access and manage GCP services and resources. These APIs provide HTTP endpoints for performing operations such as creating, reading, updating, and deleting resources.
   - Developers can interact with Google Cloud APIs directly by sending HTTP requests using standard HTTP methods (GET, POST, PUT, DELETE) and handling responses in JSON format.
   - Google provides comprehensive documentation, client libraries, and code samples for each API, making it easy to integrate GCP functionality into custom applications and workflows.

6. **Third-Party Tools and Integrations**:
   - There are numerous third-party tools, libraries, and integrations available that extend the functionality of GCP and provide additional ways to interact with GCP services.
   - Examples include Terraform for infrastructure as code, Ansible for automation and configuration management, Jenkins for continuous integration and deployment, and various monitoring and logging solutions for observability and performance analysis.


