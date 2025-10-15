# Secure the Cloud

Earlier in this course, you were introduced to **cloud computing**.  
Cloud computing is a model that allows convenient and on-demand network access to a shared pool of configurable computing resources. These resources can be provisioned and released with minimal management effort or interaction with the service provider.  

Just like any other IT infrastructure, a cloud infrastructure needs to be secured. This reading addresses some of the main security considerations unique to the cloud and introduces the **shared responsibility model** used for cloud security.  

Many organizations that use cloud resources and infrastructure express concerns about the privacy of their data and resources. This concern is addressed through cryptography and additional security measures, which will be discussed later in this course.  

---

## Cloud Security Considerations  

Organizations choose cloud services for their ease of deployment, speed, cost savings, and scalability. However, cloud computing introduces unique security challenges that cybersecurity analysts need to understand.  

### Identity Access Management (IAM)  
IAM is a collection of processes and technologies that helps organizations manage digital identities in their environment. IAM authorizes how users can access and use different cloud resources.  
- A common risk is **loose configuration of user roles**, which can allow unauthorized access to critical cloud operations.  

### Configuration  
The expanding cloud ecosystem introduces complexity to network management. Each cloud service must be **properly configured** to maintain security and compliance.  
- **Misconfigurations** are a frequent source of cloud breaches.  
- Particular care is needed during **cloud migrations**, when improperly configured processes can expose vulnerabilities.  

### Attack Surface  
Cloud providers (CSPs) offer many low-cost applications and services. Each additional service increases the organization’s **attack surface**.  
- Larger attack surface = more entry points for attackers.  
- Correct network design can mitigate these risks.  
- CSP services are generally more secure and heavily tested compared to traditional on-premises networks.  

### Zero-Day Attacks  
A **zero-day attack** is an exploit that was previously unknown.  
- CSPs are more likely to discover and patch zero-day attacks quickly.  
- They can patch hypervisors and migrate workloads automatically to prevent customer impact.  
- Organizations should also patch at the OS level to reduce exposure.  

### Visibility and Tracking  
Organizations often worry about reduced visibility in the cloud compared to on-premise networks.  
- Cloud visibility is provided through **flow logs and packet mirroring**.  
- CSPs restrict direct monitoring of their infrastructure, but they use **third-party audits** to prove security.  
- Organizations must still monitor their own configurations and ensure compliance.  

### Things Change Fast in the Cloud  
CSPs frequently update services and infrastructure, which can require changes from organizations.  
- Configurations may need updates following CSP changes.  
- Organizations may need to adapt their processes to remain secure and compliant.  

---

## Shared Responsibility Model  
The **shared responsibility model** defines which security responsibilities belong to the CSP and which belong to the customer.  

- **CSP Responsibility:** Securing the cloud infrastructure (data centers, hypervisors, host operating systems).  
- **Customer Responsibility:** Securing assets and processes operated within the cloud (applications, data, configurations).  

A common issue arises when organizations assume the CSP is responsible for securing areas that are actually the customer’s responsibility — for example, application security and service configurations.  

---

## Key Takeaways  
- Cloud computing provides flexibility and scalability but introduces unique security considerations.  
- Organizations must understand the **shared responsibility model**: CSPs secure the infrastructure, while organizations secure their own applications, data, and configurations.  
- Proper configuration, IAM, and security best practices are essential for cloud security.  

---
