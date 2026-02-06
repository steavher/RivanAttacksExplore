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

* Under _RivanVMs or on your Downloads folder on D: Drive or C: Drive, Find the OTRS-ELK.v3, open the .vmx file
* If it is not yet extracted we need to extract it to get the .vmx file
* Under _RivanVMs or on your Downloads folder on D: Drive or C: Drive, Find the OTRS-ELK.v3
* then right click on the folder, then select winrar or any other extractor and click extract to*
<img width="789" height="542" alt="image" src="https://github.com/user-attachments/assets/efdd38c3-144d-4396-8b0d-3746ca75d0d2" />

<img width="308" height="287" alt="image" src="https://github.com/user-attachments/assets/78639aeb-928b-4ddb-96de-984fd8aa24e1" />

* Next is opening the .vmx file, double click the .vmx file to open it on VMware
<img width="675" height="368" alt="image" src="https://github.com/user-attachments/assets/14719c06-b135-4dc0-b3ae-e417efdb14e8" />


# Step 2: Powering ELK-Stack and OTRS Ticketing System
* Click Power on this virtual machine, don't forget to check if the Network adapter is set to "NAT"
* If there is a pop-up that the virtual machine is being used just click "Take Ownersship" and if the virtual machine has been moved or copied just click "I copied it"
<img width="1024" height="420" alt="image" src="https://github.com/user-attachments/assets/41644471-d52f-4e31-8bf8-7673154e34a4" />

* Next is logging in on the ELK-STACK, the username and password is root:C1sc0123
<img width="1225" height="597" alt="image" src="https://github.com/user-attachments/assets/a0891d5a-ec6f-4e2f-9f94-ebf51a25315f" />



# Step 2.1: Pre-Requisites - enabling Daemon, Cron, and Mailhog processes
* In the OTRS-ELK.v3 VMware environment, the OTRS Daemon, Cron, and MailHog services must be enabled to support email processing and background operations.
* * OTRS Daemon handles background tasks such as ticket processing, notifications, and email handling.
* *Cron executes scheduled system and maintenance tasks required by OTRS.
* * MailHog provides a local SMTP service for capturing and testing outgoing emails in the lab environment.
* These services are required to ensure proper email sending/receiving and automated task execution before continuing with further configuration.

Use the Following commands to execute the process:

* Change Directory to /opt/otrs 
```bash
cd /opt/otrs/
```
<img width="366" height="81" alt="image" src="https://github.com/user-attachments/assets/88c0320c-fc81-4bbf-929f-7c5ca2dc2abc" />

* Then start the Daemon process and Cron Job using the commands below:
```bash
su -c "bin/otrs.Daemon.pl start" -s /bin/bash otrs
```
<img width="721" height="116" alt="image" src="https://github.com/user-attachments/assets/e19c29d4-ec03-45b5-a1e4-bed3ea0e940d" />

```bash
su -c "bin/Cron.sh start" -s /bin/bash otrs
```
<img width="658" height="84" alt="image" src="https://github.com/user-attachments/assets/2f892ee1-6593-416e-a301-b61436217110" />

* Finally access the mailhog
* After accessing mailhog, we will not be typing or accessing anymore of the VMWare we will not access our TUNAY na PC
```bash
mailhog
```
<img width="597" height="169" alt="image" src="https://github.com/user-attachments/assets/68b9529e-a59b-4a28-ae89-0d9b5f100334" />


# Step 2.3: Editing the IP Address to make it a DNS type of Address
* on your system, we can edit the IP address to make it look more a real-world like SOC
* On your Drive Navigate to this link "c:\Windows\System32\drivers\etc"
<img width="1137" height="347" alt="image" src="https://github.com/user-attachments/assets/6f3fed9b-8544-4d53-bdab-1ab36f7ff3bc" />

* Then right click on hosts file and select either edit with notepad or notepad++
<img width="628" height="422" alt="image" src="https://github.com/user-attachments/assets/45c902bd-8671-4312-b34e-19a6acb12663" />

* We can then add the IP Address of the given IP Address of linux to change the DNS of it, to our liking for example:
* after changing the name, save it and access the GUI of the ticketing system
<img width="675" height="450" alt="image" src="https://github.com/user-attachments/assets/77c13fbe-47a3-4c9c-bc6f-9e44e17d839f" />


# Step 3: Accessing GUI of Ticketing System and Mailhog
* Type the command to show the list of ipv4 addressses, and remember the et0 network adapter
```bash
ip -4 addr
```
<img width="864" height="175" alt="image" src="https://github.com/user-attachments/assets/4998775c-44fe-412b-b688-cf474c1afd2b" />


# Step 3.2: Znuny OTRS Ticketing System
* Access the Index and Customer Dashboard for ticketing system
```bash
http://208.8.8.146/otrs/index.pl?
```
or
```bash
http://socir.ticket.com/otrs/index.pl?
```

* The user and password for the index is root@localhost:C1sc0123, then click enter or login
* We also have users for L1 - L3 agents, we will access this later for ticket handling and ticket escalating process
* We need to use the admin user which is root@localhost to add services, types, queues, etc.
```bash
l1.agent
C1sc0123
```
```bash
l2.agent
C1sc0123
```
```bash
l3.agent
C1sc0123
```
<img width="1913" height="650" alt="image" src="https://github.com/user-attachments/assets/91fcdfd2-3f52-45bd-8d1a-e3bf564eef08" />

<img width="1906" height="947" alt="image" src="https://github.com/user-attachments/assets/fa82b950-3d26-41fc-b459-cd5a9a73b073" />

<hr>

```bash
http://208.8.8.146/otrs/customer.pl
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

* Group - Under SOC-L1
* First Response Time: 15 minutes

* * Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

* * Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

* * Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then Click save
<img width="1212" height="791" alt="image" src="https://github.com/user-attachments/assets/b7444e0d-7fd0-42e1-928f-79ef75be0811" />

<img width="383" height="178" alt="image" src="https://github.com/user-attachments/assets/18bb35c6-8acb-4d41-a3ad-86fc8e78bed7" />


## Tier 2 – Incident Responder (Investigation & Escalation)

* This queue is used for incidents escalated from Tier 1 that require deeper investigation and response.

* Escalation Settings (SLA Behavior)
* Escalation rules were configured to enforce timely incident handling:
* Group - Under SOC-L2
* First Response Time: 15 minutes

* * Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

* * Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

* * Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then click Save

<img width="1252" height="785" alt="image" src="https://github.com/user-attachments/assets/f90da185-74d9-47a6-9053-2bb98734f9df" />

<img width="408" height="191" alt="image" src="https://github.com/user-attachments/assets/92512890-61f2-4dc0-b000-6c97e7cd4995" />


## L3 – Threat Hunter / Forensics Expert

* This queue is used for advanced analysis of incidents that require threat hunting or forensic investigation beyond standard incident response.
* Escalation Settings (SLA Behavior)
* Escalation rules were configured to enforce timely incident handling:
* Group - Under SOC-L3
* First Response Time: 15 minutes

* * Ensures that alerts are acknowledged quickly after ticket creation.

* Update Time: 15 minutes

* * Requires analysts to provide status updates while the ticket is being investigated.

* Solution Time: 60 minutes

* * Defines the expected time to resolve or escalate the ticket to the next SOC tier.

* Then click Save

<img width="1326" height="805" alt="image" src="https://github.com/user-attachments/assets/65c24a07-6929-412e-909d-8fc887d51b3c" />


<img width="385" height="162" alt="image" src="https://github.com/user-attachments/assets/36920e3f-f504-4b69-9750-850d3140ea2a" />


### We can then check if it makes the changes
* On admin side
<img width="1610" height="245" alt="image" src="https://github.com/user-attachments/assets/fd983ad3-4ff2-43b4-9289-06d12a6fabff" />

* On customer side
<img width="557" height="366" alt="image" src="https://github.com/user-attachments/assets/1ad9de30-8e68-4b88-8da1-9051b8565a87" />

# Step 7: Adding and Configuring Templates 0 - 5/6
* Response templates were created in the OTRS Admin Panel to standardize ticket communication at each SOC escalation level. These templates allow analysts to send consistent and professional responses without manually typing messages.

* Templates were created from Level 0 (auto reply) up to Level 5/6 (management and resolution).
* Navigate to Admin → Template Management → Add Template

<img width="1415" height="784" alt="image" src="https://github.com/user-attachments/assets/cda8fa65-5369-4b6e-ad6e-f0eeef90b999" />


* Click add template
<img width="602" height="267" alt="image" src="https://github.com/user-attachments/assets/0954fec3-d62f-44a3-a3fd-19f3db6abdb1" />


* Create Template 0
* Under Type, select:
* * Answer

* Under Name, enter:
* * Template 0 – Auto Reply

* In the Template Content field, enter the following message:
```bash
Hello,

Your ticket has been received by the Service Desk.
Our team is currently reviewing the issue and will provide updates shortly.

Thank you.
```

* Set Validity to:
* * valid

* Click Save
<img width="1326" height="618" alt="image" src="https://github.com/user-attachments/assets/1ec804d6-9ccf-45e1-8a77-39c9e377e5d5" />


* After that select only L1 because it is linked to the template 0 - auto reply, for best practice do not select them all, after that click save and finish
Template 0 (Auto Reply) was linked only to the Tier 1 queue to ensure users receive a single acknowledgement upon ticket creation.
<img width="429" height="261" alt="image" src="https://github.com/user-attachments/assets/cc719a7d-561c-4270-b1cb-5273e4060e31" />

## Step 7.2 Creating Template 1 – Initial Analysis (Tier 1)
* Template 1 is used to inform the user that their ticket is undergoing initial analysis and triage by the Tier 1 SOC team.
* Navigate to Admin → Template Management → Add Template

* Under Type, select:
* * Answer

* Under Name, enter:
* * Template 1 – Initial Analysis

* In the Template Content field, enter the following message:
```bash
Hello,

We are currently reviewing your reported issue and performing initial analysis.
At this stage, we are validating the alert and checking for any immediate risks.

We will provide an update once this process is complete.

Thank you.
```

* Set Validity to:
* * valid

* Click Save
<img width="1383" height="608" alt="image" src="https://github.com/user-attachments/assets/11d5b53c-d5ce-45e2-8160-8ba695d28d83" />

* Queue Assignment
* Link this template to the following queue:
✔ L1 – Alert Analyst
Do NOT assign this template to higher tiers
* After that click save and finish
<img width="436" height="256" alt="image" src="https://github.com/user-attachments/assets/2cb22a74-2994-44cf-8813-b798725ec2bf" />

## Step 7.3: Creating Template 2 – Investigation Ongoing (Tier 2)
* Template 2 is used to notify the user that the ticket has been escalated to Tier 2 for deeper investigation and incident response.
* Navigate to Admin → Template Management → Add Template

* Under Type, select:
* * Answer

* Under Name, enter:
* * Template 2 – Investigation Ongoing

* In the Template Content field, enter the following message:
```bash
Hello,

Your ticket has been escalated for further investigation.
Our team is analyzing relevant logs and systems to determine the root cause of the issue.

We will provide updates as the investigation progresses.

Thank you.
```

* Set Validity to:
* * valid

* Click Save
<img width="1505" height="667" alt="image" src="https://github.com/user-attachments/assets/148428a0-2e74-4667-8f1e-02524e828ae1" />

* Queue Assignment
* Link this template to the following queue:
✔ L2 – Incident Responder
* Do NOT assign this template to other queues
* Purpose in Workflow
* * Informs the user of escalation
* * Sets expectation for deeper analysis
* * Aligns communication with SOC escalation flow
* Then click Save and finish
<img width="457" height="279" alt="image" src="https://github.com/user-attachments/assets/e185e8f7-5db7-44ca-9868-f2d9d24b7f2a" />


## Step 7.4: Creating Template 3 – Advanced Analysis / Resolution (Tier 3)
* Template 3 is used when a ticket reaches Tier 3 for advanced analysis or final resolution. This may involve threat hunting, forensic review, or confirmation that no further action is required.
* Navigate to Admin → Template Management → Add Template

* Under Type, select:
* * Answer

* Under Name, enter:
* * Template 3 – Advanced Analysis / Resolution

* In the Template Content field, enter the following message:
```bash
Hello,

Your ticket is currently undergoing advanced analysis.
Our security team is reviewing the findings and applying final actions as needed.

You will be notified once the analysis is completed or the issue is resolved.

Thank you.
```
* Set Validity to:
* * valid

* Click Save
<img width="1439" height="659" alt="image" src="https://github.com/user-attachments/assets/b31a04a4-d318-4064-aa89-7fbcf8618768" />

* Queue Assignment

* * Link this template to the following queue:
✔ L3 – Threat Hunter / Forensics Expert
* Do NOT assign this template to other queues

* Purpose in Workflow
* * Communicates advanced investigation status
* * Indicates final-stage handling
* * Keeps user informed without exposing technical details
  * Click save and finish
<img width="531" height="274" alt="image" src="https://github.com/user-attachments/assets/fe11ffe9-fa12-4777-998e-017e16e14b1b" />

* Overview of added templates and queues
<img width="1618" height="233" alt="image" src="https://github.com/user-attachments/assets/0ab0850c-ef36-42e7-9393-7d14c3ec6a37" />

# Step 8: Creating Ticket 2nd run
* On Customer Side Panel, Create again your 1st ticket
* click "Create your 1st ticket"
<img width="574" height="257" alt="image" src="https://github.com/user-attachments/assets/f81c37ac-9e5e-40b7-b282-0cc20c995c7e" />

* On type, select Phishing Email Reports
<img width="409" height="226" alt="image" src="https://github.com/user-attachments/assets/5f9ef216-f06c-4deb-8689-87cfee8f40fa" />


* Send it to: "L1 - Alert Analyst"
<img width="396" height="184" alt="image" src="https://github.com/user-attachments/assets/ebe5fa70-3285-4408-9538-9f18aff4fcd8" />


* Subject (example):
```
Suspicious Email Received – Possible Phishing
```

Text (example content):
``` bash
Good day,

I received an email claiming to be from our IT department asking me to click a link and verify my account.

The email looks suspicious and may be a phishing attempt.
Please investigate.

Thank you.
```

* Leave these EMPTY for now:

* * Service

* * SLA

* Click Submit

✅ Ticket will be created

✅ Template 0 (Auto Reply) should trigger

✅ Ticket should land in L1 – Alert Analyst

<img width="1177" height="753" alt="image" src="https://github.com/user-attachments/assets/a4f85cb5-a4c1-4706-ae2d-3a7b4ddbb6f2" />

* After submitting the ticket, the ticket can now be seen to the customer or user
<img width="1907" height="234" alt="image" src="https://github.com/user-attachments/assets/4a8fcc25-4dc4-4190-9ce1-8217f2cba6fc" />

# Step 9: Verifying and Applying Template
* For demonstration purposes, a single administrative agent account was used to simulate L1, L2, and L3 SOC roles. Tickets were manually routed between queues to demonstrate escalation workflows.
* Under Index panel → Tickets → Queues

<img width="957" height="483" alt="image" src="https://github.com/user-attachments/assets/b29d206f-009a-4cad-a274-78afeee0d3d7" />

* Then Click the L1 - Alert Ticket
<img width="601" height="318" alt="image" src="https://github.com/user-attachments/assets/865113a5-fc6e-4d96-a9df-f0ff8adcd08a" />
<img width="1904" height="647" alt="image" src="https://github.com/user-attachments/assets/2a7a49fc-cc8d-4aac-b701-8da0461af1ee" />

## Step 9.3: Applying Template 0 - Auto Reply
* This step demonstrates how the Service Desk or SOC analyst applies the appropriate response template during the early stage of ticket handling.
* We can now then apply the appropriate template by clicking the reply button and the blank message
* But in Real-World Situations, tickets are automatically will receive an email or an corresponding message whatever the siuation is. For that we will Continue to add auto response to our ticketing system.
<img width="1464" height="589" alt="image" src="https://github.com/user-attachments/assets/fe752198-916a-4b5d-8860-e1245a169fad" />

## Sub-Step 9.4: Configuring Auto Response aka Template 0 - Auto Reply
* Create a True Auto Response (System-Level)
* Go to:
* * Admin → Auto Responses → Add Auto Response
<img width="1003" height="422" alt="image" src="https://github.com/user-attachments/assets/a3fb4fec-311e-483a-a3dc-9a5ca4cebc9c" />

<img width="338" height="184" alt="image" src="https://github.com/user-attachments/assets/0a383f2e-b3a0-4810-b057-ff1d2d0274c7" />

* Configure as follows:
* Name:
```
Auto Reply – Ticket Received
```

* Subject:
```
[Ticket#<OTRS_TICKET_TicketNumber>] Ticket Received
```

* Response Body:
```
Hello,

Your ticket has been successfully received by the Security Operations Center.

Our team is currently reviewing the issue and will provide updates as soon as possible.

Please do not reply to this message unless additional information is required.

Thank you,
SOC Team
```

* Type - auto reply
* Validity:
✔ valid

➡ Click Save
<img width="1507" height="718" alt="image" src="https://github.com/user-attachments/assets/62b31401-c4e4-4a8c-a150-ed4cdb5d0c67" />


## Sub-Step 9.4: Assign Auto Response to L1 Queue (CRITICAL)
* Go to Admin → Queues → L1 – Alert Analyst
<img width="726" height="571" alt="image" src="https://github.com/user-attachments/assets/ef360851-a52b-4e96-bf51-d808169be53c" />

* Under Related Actions, find "Queues → Auto Responses :
<img width="277" height="543" alt="image" src="https://github.com/user-attachments/assets/38a2318f-2669-4f1f-a1e2-cd2cbce54106" />


* Then Click "L1 - Alert Analyst":
<img width="806" height="215" alt="image" src="https://github.com/user-attachments/assets/ce5affb3-83c4-4cb2-9c68-88eb2d510ede" />

* Configure:
auto reply: Auto Reply – Ticket Received
➡ Click Save and finish
<img width="1014" height="269" alt="image" src="https://github.com/user-attachments/assets/a087d6f1-69dd-42b6-8f7e-e244d4d4ff18" />

## Re-continouing Sub-Step 9.2.2: Automatic Acknowledgement or automatic reply upon ticket creation
* Configure as follow to have an auto reply
* On the customer side, recreate another ticket, then click submit
<img width="350" height="189" alt="image" src="https://github.com/user-attachments/assets/0f876157-cd79-4210-87f6-e85aea813dc6" />

<img width="1594" height="802" alt="image" src="https://github.com/user-attachments/assets/412c7ee1-db34-40e1-a5a9-7b5852e3bd11" />

* After submitting, you will then receive an auto response by the system
<img width="1642" height="887" alt="image" src="https://github.com/user-attachments/assets/2a7cc888-f1bf-4f88-b1db-0c606ef3a7fb" />

# Step 9.4: Applying Template 1 on L1 - Alert Analysis: 
* We can now then apply the appropriate template by clicking the reply button and the blank message
* Under Tickets -> click the given ticket and select template 1 - Initial Analysis
* From there another TAB will automatically open and click the -> send mail button
<img width="1416" height="795" alt="image" src="https://github.com/user-attachments/assets/3b0bbd15-bb40-47eb-a572-4d9c8c9c58d7" />
