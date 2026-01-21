<div align="center">
  <img src="https://github.com/user-attachments/assets/e4d90e60-ee23-4e28-b9c1-ab35e68fed13" alt="Rivan Cyber Training Institute Logo" width="200">
  <h1>RIVAN CYBER TRAINING INSTITUTE</h1>
</div>

<hr>

# Step 1: Opening VMware
* Open the Vmware APP on your pc, press ⊞ Windows key and type "Vmware"
<img width="760" height="565" alt="image" src="https://github.com/user-attachments/assets/21ae72ab-07f9-4f55-bd73-31fdf9fa742a"/>


# Step 2: Opening _D3Pentest VMware File
* Under the File Button, Click the Open button
<img width="1135" height="490" alt="image" src="https://github.com/user-attachments/assets/86f26c5c-357f-4553-a494-62bf66868e61" />

<hr>

* Under _RivanVMs folder on D: Drive or C: Drive, Find the _D3PentestVM and open the .vmx file
<img width="777" height="431" alt="image" src="https://github.com/user-attachments/assets/995121ca-795f-470e-a880-18d811c01c1f" />


# Step 3: Changing the Network Adapter to Host Only via Custom VMnet1
* Click "Edit virtual Machine Settings"
<img width="545" height="387" alt="image" src="https://github.com/user-attachments/assets/b392f77d-56dd-4ffe-ab41-3a0249180b91" />

<hr>

* Change Network Adapter NAT to Custom VMnet 1
<img width="620" height="602" alt="image" src="https://github.com/user-attachments/assets/15b489de-08db-47ad-bc30-405fbca6a068" />

<hr>

* Then Click Okay
<img width="767" height="740" alt="image" src="https://github.com/user-attachments/assets/12b51e83-2a1c-481e-8be2-7bf81e30bc5d" />

# Step 4: Powering On the Virtual Machine
* 1st click the Power on this Virtual machine, If there is a pop-up if the virtual machine has been moved or copied just click "I copied it"
<img width="367" height="207" alt="image" src="https://github.com/user-attachments/assets/00657994-fa2f-4e51-a8d5-57335726f464" />

<hr>

* After clicking the Power on this Virtual machine and click inside the virtual machine and click Enter, you must be quick during this process or else you will receive a black screen
<img width="837" height="627" alt="image" src="https://github.com/user-attachments/assets/3f95f25d-7bbc-417d-a157-4b3ac31b4136" />

# Step 5: Accessing Kali-Linux
* Both username and password is "kali"
<img width="584" height="375" alt="image" src="https://github.com/user-attachments/assets/ca7863da-2621-493b-8f49-a678478fdd77" />
<img width="1919" height="958" alt="image" src="https://github.com/user-attachments/assets/3c393b7d-73bb-4522-a1c0-b09057127692" />


<hr>

# Step 6: Accessing CLI Linux on SecureCRT
* This is essential for easy copy and paste, that way we don't have to open kali-linux GUI just the CLI of it.
* On Kali-linux VMware open the terminal and type the command
```bash
ip address
```
<img width="1441" height="757" alt="image" src="https://github.com/user-attachments/assets/188e1ccc-660e-46f3-acb2-0c83792cda8d" />

<hr>

* Remember the 2nd network adapter, which is eth0, it may differ to each and everyone so remember the IP Address
<img width="687" height="537" alt="image" src="https://github.com/user-attachments/assets/d22d5847-28d5-42d1-b687-882210c9092f" />

## Step 6.2: Accessing CLI Linux on SecureCRT 2.0
* On TUNAY na PC, open SecureCRT, then click the Kidlat icon
<img width="1056" height="613" alt="image" src="https://github.com/user-attachments/assets/fa1093ee-aabb-45f8-b9f5-24f203539143" />

* Input the IP Address of Kali-Linux, which is eth0, then click Connect
<img width="407" height="412" alt="image" src="https://github.com/user-attachments/assets/6fdd488c-667f-4b84-88c6-5448ce5b251e" />

* If there is the New Host Key, Accept it click Accept Once
<img width="1018" height="504" alt="image" src="https://github.com/user-attachments/assets/ff291cbe-a6f5-4a9d-8c5f-34b76d041cc4" />

* After that input the username and password which is kali:kali
<img width="371" height="196" alt="image" src="https://github.com/user-attachments/assets/31f2a9d8-6650-48b1-802c-af0dec8ce4f1" />

* We have accessed the CLI on Kali-Linux
<img width="793" height="263" alt="image" src="https://github.com/user-attachments/assets/c04aef13-aa1b-4ea6-b7a6-c9c7d2edd12b" />


<hr>

# Step 7: Starting xampp and stopping apache
* These commands stop Kali’s default Apache service and start XAMPP’s Apache and MySQL services to avoid port conflicts and ensure XAMPP handles the web environment.
* each line is separate, so copy the 1st line and paste it on SecureCRT on CLI of kali-Linux
```bash
sudo /opt/lampp/lampp start
```
<img width="342" height="98" alt="image" src="https://github.com/user-attachments/assets/87846ae4-2c99-4e54-a8b7-c67c96e687e5" />

```bash
sudo systemctl stop apache2
```
<img width="304" height="44" alt="image" src="https://github.com/user-attachments/assets/d8346bd6-f9f3-4848-a829-b105aeea997c" />


<hr>

# Step 8: Opening OWASP
* Using this IP Address or Link change the 4th octet based on the given IP Address on the Kali-Linux
```bash
http://192.168.101.___/mutillidae/src/index.php
```
<img width="1919" height="882" alt="image" src="https://github.com/user-attachments/assets/b4abde2d-ee1e-43ce-bb86-e457348ff904" />


# Step 9: Opening SQLI Injection
* This step opens the “User Info (SQL)” page in OWASP Mutillidae II, which is intentionally vulnerable to SQL Injection and allows testing of data extraction attacks.
<img width="1013" height="731" alt="image" src="https://github.com/user-attachments/assets/8aa7d7dd-5dec-4ee8-9027-14172e851bdb" />

* Create your preffered user account
<img width="876" height="394" alt="image" src="https://github.com/user-attachments/assets/4c299a07-fb32-43b7-9c0d-f77c7e066eaa" />

* Example:
* Username: Rivan
* Password: C1sc0123
* Confirm Password: C1sc0123
* Signature: Rivan Account January 21, 2026, Then Click Create Account
<img width="728" height="365" alt="image" src="https://github.com/user-attachments/assets/18846e8d-fa19-4664-99d8-503b5101deba" />
<img width="1459" height="487" alt="image" src="https://github.com/user-attachments/assets/c9396a6b-9e21-45d6-9aca-cd0f86eec302" />

<hr>

# Step 10: SQL Statements
* If a website or a code runs this SQL Statement below
```bash
SELECT * FROM users WHERE username = 'input' AND password = 'input';
```
* This SQL query retrieves user records by directly comparing user-supplied username and password values. Because the inputs are not sanitized or parameterized, the query is vulnerable to SQL Injection attacks.
* In Basic Terms, kung ano makuha sa database or kung kahit sino na nasa input na user and password makikita agad kasi hindi naka limit or naka parameterized throughly
* An Attacker could run this SQL Statement to catch all the user account within the database

```bash
' OR '1'='1
```

* Breaking down the conditions:
* username = '' is false
* '1'='1' is ALWAYS TRUE (1 always equals 1)
* password = '' is false
* Another '1'='1' is ALWAYS TRUE

<hr>

* Going back to the Activity copy the SQL Attack Statement and paste it on both Username and Password, then Click Enter or View Account Details
<img width="1666" height="750" alt="image" src="https://github.com/user-attachments/assets/29661f07-d5b3-4d2c-8639-7f7d5d538541" />

* The bottom image shows that the attack works and proves that the sql statement input must be parametized and must be limited to the user who is accessing the account to defend SQLi Injection
<img width="1230" height="701" alt="image" src="https://github.com/user-attachments/assets/ed2cd82c-1f00-45bd-b689-866fe73e0277" />


# Step 11: XML External Entities (XXE)
XXE is an attack where hackers inject malicious XML code into an application that processes XML files, tricking it into:
* Reading sensitive files (like /etc/passwd on Linux)
* Making network requests to internal systems
* Causing denial of service crashes
* Stealing data from the serverXXE is an attack where hackers inject malicious XML code into an application that processes XML files, tricking it into:
* Reading sensitive files (like /etc/passwd on Linux)
* Making network requests to internal systems
* Causing denial of service crashes
* Stealing data from the server

* Go to OWASP 2017 - A4 XML Eternal Entities - XML Validator
<img width="1026" height="674" alt="image" src="https://github.com/user-attachments/assets/a6a84a41-86af-4957-9c36-9afe12fea4df" />

* Paste this payload:
```bash
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [  
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/passwd" >]>
<foo>&xxe;</foo>
```
<img width="656" height="241" alt="image" src="https://github.com/user-attachments/assets/ffc532ed-7a5b-4316-b8ee-e98159050eb1" />

* What the payload does is executes all the hidden contents of /etc/passwd, which basically looks like the image below: now, to read this
* The long text you see IS THE CONTENTS OF /etc/passwd. Each line represents a user account on the server:
### Example Line:
### root:x:0:0:root:/root:/usr/bin/zsh
* root = Username
* x = Password placeholder (actual hashes are in /etc/shadow)
* 0 = User ID (0 = root/superuser)
* 0 = Group ID
* root = Description
* /root = Home directory
* /usr/bin/zsh = Default shell

<img width="1699" height="649" alt="image" src="https://github.com/user-attachments/assets/86bfd368-fb0a-45ce-9ec9-cd10f9c3abc5" />

* Now how to prevent this?
* DISABLE External Entities in XML Parser
* Use SAX or StAX Parsers (not DOM) when possible

# Step 12: Introduction to Honey Pot
* A honeypot is a decoy system that lures attackers to study their behavior without risking real assets.
* Open CMD on PC and nmap the given IP Address of the Kali Linux, change the 4th octet to your given IP Address
```bash
nmap -v 192.168.101.___
```
<img width="898" height="686" alt="image" src="https://github.com/user-attachments/assets/28d915cf-54ed-457e-b728-ed593c3cbe6a" />
