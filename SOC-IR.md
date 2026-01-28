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


# Step 3: Accessing GUI of Ticketing System
* Type the command to show the list of ipv4 addressses, and remember the et0 to connect it to securecrt
```bash
ip -4 addr
``` 
<img width="795" height="200" alt="image" src="https://github.com/user-attachments/assets/1f7d18bc-a012-48cc-b3e1-0fc827b3218b" />


# Step 3.2: Znuny OTRS Ticketing System
* Access the Index and Customer Dashboard for ticketing system
```bash
http://208.8.8.133/otrs/index.pl?
```
* The user and password for the index is root@localhost:C1sc0123, then click enter or login
<img width="667" height="480" alt="image" src="https://github.com/user-attachments/assets/e2bc4509-36dc-4422-9ec1-a42c4a6e945f" />
<img width="1906" height="947" alt="image" src="https://github.com/user-attachments/assets/fa82b950-3d26-41fc-b459-cd5a9a73b073" />


<hr>

```bash
http://208.8.8.133/otrs/customer.pl
```
* The user and password for the customer is user1:C1sc0123, then click enter or login
<img width="1911" height="439" alt="image" src="https://github.com/user-attachments/assets/153aa3c8-e43c-428f-851f-832adf5a254e" />
<img width="1916" height="579" alt="image" src="https://github.com/user-attachments/assets/532a925e-7b3e-4c1a-8a7c-5771cddeec71" />

# Step 4: Creating 1st Ticket
* On the Customer Panel, we have to create a ticket
* click "Create your 1st ticket"
<img width="574" height="257" alt="image" src="https://github.com/user-attachments/assets/f81c37ac-9e5e-40b7-b282-0cc20c995c7e" />


