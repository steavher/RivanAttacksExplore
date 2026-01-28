<div align="center">
  <img src="https://github.com/user-attachments/assets/e4d90e60-ee23-4e28-b9c1-ab35e68fed13" alt="Rivan Cyber Training Institute Logo" width="200">
  <h1>RIVAN CYBER TRAINING INSTITUTE</h1>
</div>

<hr>



<hr>

<div align="center">
<img width="1280" height="720" alt="1753705128100" src="https://github.com/user-attachments/assets/c1dc4f0f-5404-4ced-8e8d-5e9ae60eef6c" />
</div>


# Step 1: Opening ELK-STACK and OTRS Ticketing System
* Under the File Button, Click the Open button
<img width="1135" height="490" alt="image" src="https://github.com/user-attachments/assets/86f26c5c-357f-4553-a494-62bf66868e61" />

<hr>

* Under _RivanVMs or on your Downloads folder on D: Drive or C: Drive, Find the ELK-OTRS.V1 or ELK-OTRS.v2 either way its fine, open the .vmx file
* If it is not yet extracted we need to extract it to get the .vmx file
* Under _RivanVMs or on your Downloads folder on D: Drive or C: Drive, Find the ELK-OTRS.V1 or ELK-OTRS.v2 either way its fine
* then right click on the folder, then select winrar or any other extractor and click extract to*
<img width="687" height="199" alt="image" src="https://github.com/user-attachments/assets/5ee97301-7222-4acc-a5dd-39d5f54ed735" />
<img width="302" height="271" alt="image" src="https://github.com/user-attachments/assets/1a065f4d-e022-4c6f-bdb2-e4b94908a815" />

* Next is opening the .vmx file, double click the .vmx file to open it on VMware
<img width="627" height="45" alt="image" src="https://github.com/user-attachments/assets/12cf9883-6ea6-47a0-a669-a833a8bdc47f" />


<img width="616" height="283" alt="image" src="https://github.com/user-attachments/assets/3824283a-a102-4e6c-befe-f5c0138ba1a3" />

# Step 2: Powering ELK-Stack and OTRS Ticketing System
* Click Power on this virtual machine, don't forget to check if the Network adapter is set to "NAT"
* If there is a pop-up if the virtual machine has been moved or copied just click "I copied it"
<img width="590" height="480" alt="image" src="https://github.com/user-attachments/assets/6bd0bc9a-b726-48e0-b52d-8232339f1105" />

<img width="378" height="208" alt="image" src="https://github.com/user-attachments/assets/c0ae620e-f575-47df-92ca-adc191eadded" />

* Next is logging in on the ELK-STACK, the username and password is root:C1sc0123
<img width="656" height="338" alt="image" src="https://github.com/user-attachments/assets/21e2398c-e292-463b-9304-f075cba9cbdc" />


# Step 2.2: Editing the IP Address to make it a DNS type of Address
* on your system, we can edit the IP address to make it look more a real-world like SOC
* On your Drive Navigate to this link "c:\Windows\System32\drivers\etc"
<img width="1137" height="347" alt="image" src="https://github.com/user-attachments/assets/6f3fed9b-8544-4d53-bdab-1ab36f7ff3bc" />

* Then right click on hosts file and select either edit with notepad or notepad++
<img width="628" height="422" alt="image" src="https://github.com/user-attachments/assets/45c902bd-8671-4312-b34e-19a6acb12663" />

* We can then add the IP Address of the given IP Address of linux to change the DNS of it, to our liking for example:
* after changing the name, save it and access the GUI of the ticketing system
<img width="935" height="635" alt="image" src="https://github.com/user-attachments/assets/a23f198b-16d7-456d-ba85-b1d0d40738c9" />


# Step 3: Accessing GUI of Ticketing System
* Type the command to show the list of ipv4 addressses, and remember the et0 network adapter
```bash
ip -4 addr
```


# Step 3.2: Znuny OTRS Ticketing System
* Access the Index and Customer Dashboard for ticketing system
```bash
http://208.8.8.133/otrs/index.pl?
```
or
```bash
http://socir.ticket.com/otrs/index.pl?
```

* The user and password for the index is root@localhost:C1sc0123, then click enter or login
<img width="1913" height="650" alt="image" src="https://github.com/user-attachments/assets/91fcdfd2-3f52-45bd-8d1a-e3bf564eef08" />

<img width="1906" height="947" alt="image" src="https://github.com/user-attachments/assets/fa82b950-3d26-41fc-b459-cd5a9a73b073" />


<hr>

```bash
http://208.8.8.133/otrs/customer.pl
```
or
```bash
http://socir.ticket.com/otrs/customer.pl
```
* The user and password for the customer is user1:C1sc0123, then click enter or login
<img width="1914" height="691" alt="image" src="https://github.com/user-attachments/assets/38965a9c-e11c-4e1b-91d5-dd49fe0d3d10" />

<img width="1916" height="579" alt="image" src="https://github.com/user-attachments/assets/532a925e-7b3e-4c1a-8a7c-5771cddeec71" />

# Step 4: Creating 1st Ticket aka at Service Desk
* On the Customer Panel, we have to create a ticket
* click "Create your 1st ticket"
* at 1st creating tickets on customer panel, itsome of the panels or selection of types, sending it to, service and Service Level Agreement are not yet configured so we have to configure it through admin by adding all levels and incidents.

<img width="574" height="257" alt="image" src="https://github.com/user-attachments/assets/f81c37ac-9e5e-40b7-b282-0cc20c995c7e" />

<img width="388" height="175" alt="image" src="https://github.com/user-attachments/assets/22b37d73-c2a5-42cf-ba68-e0a1c2eac4b8" />

<img width="367" height="111" alt="image" src="https://github.com/user-attachments/assets/e75278d8-ada3-4304-a6bb-73db78dbb947" />

<img width="363" height="56" alt="image" src="https://github.com/user-attachments/assets/c50243a1-4ad3-424a-938c-61b269504e0e" />


# Step 5: Adding and Managing Ticket Types
* On the Admin Side, we can add and manage ticket
* Ticket types are managed through the Admin Panel and are used to define how incidents are categorized within the system. These types help structure ticket handling and ensure consistent incident classification.
* Access the Admin Panel
* Navigate to Ticket Settings / Types
<img width="1615" height="788" alt="image" src="https://github.com/user-attachments/assets/91e774f2-573f-4eaf-9316-cf41b37c1e23" />

* Add or modify ticket types based on operational or security needs
<img width="1672" height="351" alt="image" src="https://github.com/user-attachments/assets/c7cb395b-296e-44f4-9494-ee91aedd6bf7" />


1. Phishing Email Reports
Description: Users report suspicious emails that may contain malicious links or attachments. These emails often impersonate legitimate services or internal contacts.
SOC Task: Analyze the email headers, URLs, and attachments; sandbox suspicious content; block the sender or domain; educate the user.
* Save and apply changes to make the types available in the Customer Panel

<img width="1254" height="262" alt="image" src="https://github.com/user-attachments/assets/32800c2f-941a-4e2a-868e-330afce87c67" />



2. Endpoint Malware Detection
Description: Antivirus or EDR solutions detect malware (e.g., Trojans, ransomware, adware) on user endpoints.
SOC Task: Investigate the detection; isolate the device if necessary; analyze the malware behavior; initiate remediation steps.
* Save and apply changes to make the types available in the Customer Panel

<img width="1211" height="249" alt="image" src="https://github.com/user-attachments/assets/43e31c41-3eb8-4049-a722-7285553ab1f9" />



3. Suspicious Login Activity
Description: Unusual or impossible logins (e.g., logins from different countries within minutes) are flagged by the SIEM or IAM solution.
SOC Task: Verify if login is legitimate or compromised; reset credentials; analyze source IP and geolocation; apply MFA if not enabled.
* Save and apply changes to make the types available in the Customer Panel

<img width="1161" height="202" alt="image" src="https://github.com/user-attachments/assets/647bcc30-e770-44ce-afc0-cf6f7f4bec13" />

* We can then Confirm this on the added types on the admin or on the customer side
* Admin Side
<img width="1904" height="362" alt="image" src="https://github.com/user-attachments/assets/e98154e8-1660-446e-991c-30b4db737e46" />

* Customer Side
<img width="532" height="384" alt="image" src="https://github.com/user-attachments/assets/b2546959-0aa9-4ee2-9e7a-d83c035bfc47" />



# Step 6: Adding and Configuring Queues (SOC Tier Structure)
* Queues were created in the OTRS Admin Panel to simulate a multi-tier Security Operations Center (SOC) workflow. Each queue represents a specific SOC role responsible for handling incidents at different levels of complexity.

* This setup demonstrates how tickets are triaged, escalated, and resolved in real-world security operations.
* On the Admin Panel, click Admin and click Queues
<img width="960" height="619" alt="image" src="https://github.com/user-attachments/assets/492df1b0-c9b8-4d35-bb3f-c4f0ddce2331" />

* Add Queues
<img width="1716" height="318" alt="image" src="https://github.com/user-attachments/assets/e8ecde25-9e12-4252-b47b-292590cfde72" />

* Input this info:

## L1 – Alert Analyst (Frontline / Monitoring & Triage)

* This queue is used for initial alert monitoring and triage. All newly created security-related tickets are first assigned to this queue.

* Escalation Settings (SLA Behavior)
* Escalation rules were configured to enforce timely incident handling:

* First Response Time: 15 minutes

Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then Click save
<img width="1471" height="818" alt="image" src="https://github.com/user-attachments/assets/717f50b0-89f5-43da-9568-ed1bf83cb4fc" />
<img width="383" height="178" alt="image" src="https://github.com/user-attachments/assets/18bb35c6-8acb-4d41-a3ad-86fc8e78bed7" />


## Tier 2 – Incident Responder (Investigation & Escalation)

* This queue is used for incidents escalated from Tier 1 that require deeper investigation and response.

* Escalation Settings (SLA Behavior)
* Escalation rules were configured to enforce timely incident handling:

* First Response Time: 15 minutes

Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then click Save

<img width="1233" height="802" alt="image" src="https://github.com/user-attachments/assets/3913df5e-3c07-4565-98f1-27de607b22c3" />

<img width="408" height="191" alt="image" src="https://github.com/user-attachments/assets/92512890-61f2-4dc0-b000-6c97e7cd4995" />


## L3 – Threat Hunter / Forensics Expert

* This queue is used for advanced analysis of incidents that require threat hunting or forensic investigation beyond standard incident response.
* Escalation Settings (SLA Behavior)
* Escalation rules were configured to enforce timely incident handling:

* First Response Time: 15 minutes

Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then click Save

<img width="1298" height="790" alt="image" src="https://github.com/user-attachments/assets/2beeec2d-8b76-4413-8d30-1fd49c0bb832" />

<img width="385" height="162" alt="image" src="https://github.com/user-attachments/assets/36920e3f-f504-4b69-9750-850d3140ea2a" />


### We can then check if it makes the changes
* On admin side
<img width="1610" height="245" alt="image" src="https://github.com/user-attachments/assets/fd983ad3-4ff2-43b4-9289-06d12a6fabff" />

* On customer side
<img width="557" height="366" alt="image" src="https://github.com/user-attachments/assets/1ad9de30-8e68-4b88-8da1-9051b8565a87" />

# Step 7: Adding and Configuring Templates
* Response templates were created in the OTRS Admin Panel to standardize ticket communication at each SOC escalation level. These templates allow analysts to send consistent and professional responses without manually typing messages.

* Templates were created from Level 0 (auto reply) up to Level 5/6 (management and resolution).
* On the admin page navigate through templates

<img width="1415" height="784" alt="image" src="https://github.com/user-attachments/assets/cda8fa65-5369-4b6e-ad6e-f0eeef90b999" />


* Click add template
<img width="602" height="267" alt="image" src="https://github.com/user-attachments/assets/0954fec3-d62f-44a3-a3fd-19f3db6abdb1" />
