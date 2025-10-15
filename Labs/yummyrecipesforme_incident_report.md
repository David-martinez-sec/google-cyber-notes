# Incident Report: Website Compromise – yummyrecipesforme.com

## Scenario
You are a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A former employee has decided to lure users to a fake website with malware.

The former employee/hacker executed a brute force attack to gain access to the web host. They repeatedly entered several known default passwords for the administrative account until they correctly guessed the right one. After they obtained the login credentials, they were able to access the admin panel and change the website’s source code. They embedded a JavaScript function in the source code that prompted visitors to download and run a file upon visiting the website. After embedding the malware, the hacker changed the password to the administrative account. When customers download the file, they are redirected to a fake version of the website that contains the malware.

Several hours after the attack, multiple customers emailed yummyrecipesforme’s helpdesk. They complained that the company’s website had prompted them to download a file to access free recipes. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly.

In response to this incident, the website owner tries to log in to the admin panel but is unable to, so they reach out to the website hosting provider. You and other cybersecurity analysts are tasked with investigating this security event.

To address the incident, you create a sandbox environment to observe the suspicious website behavior. You run the network protocol analyzer tcpdump, then type in the URL for the website, yummyrecipesforme.com. As soon as the website loads, you are prompted to download an executable file to update your browser. You accept the download and allow the file to run. You then observe that your browser redirects you to a different URL, greatrecipesforme.com, which contains the malware.

The logs show the following process:

1. The browser initiates a DNS request: It requests the IP address of the yummyrecipesforme.com URL from the DNS server.
2. The DNS replies with the correct IP address.
3. The browser initiates an HTTP request: It requests the yummyrecipesforme.com webpage using the IP address sent by the DNS server.
4. The browser initiates the download of the malware.
5. The browser initiates a DNS request for greatrecipesforme.com.
6. The DNS server responds with the IP address for greatrecipesforme.com.
7. The browser initiates an HTTP request to the IP address for greatrecipesforme.com.

A senior analyst confirms that the website was compromised. The analyst checks the source code for the website. They notice that JavaScript code had been added to prompt website visitors to download an executable file. Analysis of the downloaded file found a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com.

The cybersecurity team reports that the web server was impacted by a brute force attack. The disgruntled hacker was able to guess the password easily because the admin password was still set to the default password. Additionally, there were no controls in place to prevent a brute force attack.

Your job is to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website. You should also recommend a security action to take to prevent brute force attacks in the future.

---

## Section 1: Identify the network protocol involved in the incident
The primary protocol involved in this incident was **HTTP** at the application layer. The malicious JavaScript was embedded within the website’s source code and delivered over HTTP. This enabled the forced file download and subsequent redirection to the attacker-controlled site.

---

## Section 2: Document the incident
In response to multiple emails to the Helpdesk, we investigated reports of suspicious downloads, redirection of website traffic, and potential malware infections on customer computers. During the investigation, it was confirmed that the website owner was unable to log in to the administrative panel.

To analyze the incident, we created a sandbox environment to safely observe the website’s behavior. Using tcpdump, we visited the website and observed a download request, a redirect, and subsequent access to a malicious site. The tcpdump logs revealed that a malicious script was embedded in the website’s source code. This was evident from an immediate HTTP request triggered upon connecting to the site. Once the initial GET request completed, a new DNS request was made, and traffic was redirected to the counterfeit website. There, another HTTP GET request was issued, and malicious software was downloaded.

---

## Section 3: Recommend one remediation for brute force attacks
My immediate recommendation is to implement **multi-factor authentication (MFA)** for the website’s administrative panel. MFA significantly hardens account security by requiring an additional verification factor beyond the password, reducing the attack surface and making brute force attempts far less effective. While enforcing stronger password complexity requirements and updating password policies are valuable secondary measures, MFA provides the most robust and immediate protection for this critical asset.

---
