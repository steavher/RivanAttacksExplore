<div align="center">
  <img src="https://github.com/user-attachments/assets/e4d90e60-ee23-4e28-b9c1-ab35e68fed13" alt="Rivan Cyber Training Institute Logo" width="200">
  <h1>RIVAN CYBER TRAINING INSTITUTE</h1>
</div>

<hr>


<img width="1280" height="688" alt="1721187455024" src="https://github.com/user-attachments/assets/a41f39fa-48a7-405b-a05b-3d2daa30ddb9" />

# Step 1: Opening VMware
* Open the Vmware APP on your pc, press ⊞ Windows key and type "Vmware"
<img width="760" height="565" alt="image" src="https://github.com/user-attachments/assets/21ae72ab-07f9-4f55-bd73-31fdf9fa742a"/>

# Step 2: Opening _D3Pentest VMware File
* Under the File Button, Click the Open button
<img width="1135" height="490" alt="image" src="https://github.com/user-attachments/assets/86f26c5c-357f-4553-a494-62bf66868e61" />

<hr>

* Under _RivanVMs folder on D: Drive or C: Drive, Find the _D3PentestVM and open the .vmx file
<img width="777" height="431" alt="image" src="https://github.com/user-attachments/assets/995121ca-795f-470e-a880-18d811c01c1f" />


* Change Network Adapter Bridged to NAT and Replicate it
<img width="742" height="329" alt="image" src="https://github.com/user-attachments/assets/de0f92cf-f8ff-4d85-96ab-ec8d8be405a9" />


<hr>

* Then Click Okay
<img width="758" height="701" alt="image" src="https://github.com/user-attachments/assets/b5684fd6-8e1c-473b-be75-07a8b5b0a8d7" />


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

# Step 6.3: Become a bossing

```bash
sudo su
```

<img width="360" height="72" alt="image" src="https://github.com/user-attachments/assets/d5d3dc77-0ddd-457d-9a21-0fb945559793" />
* It Should then return as a red line and with a directory of root@kali

# Step 7: Accessing MsfConsole / Metasploit

* Input the command

```bash
msfconsole
```

<img width="607" height="231" alt="image" src="https://github.com/user-attachments/assets/72fb902e-4a72-4dea-acd3-e8eb008437e4" />

* then wait a couple seconds to boot the program

<img width="577" height="749" alt="image" src="https://github.com/user-attachments/assets/ed7b6ecb-6ae4-4587-94ae-492dade4a9a6" />

# Step 8: Adding User.txt file and Pass.txt file on kali-linux
* On the Desktop of Kali-linux, right click and select Create Document > Empty File
<img width="554" height="391" alt="image" src="https://github.com/user-attachments/assets/000ccadb-c362-4980-a58f-8be4ff9ecb55" />

* Then create user.txt and pass.txt 2 files, just like the images below:
<img width="665" height="197" alt="image" src="https://github.com/user-attachments/assets/a7daa6d7-9d00-4d6d-8eb4-8ad094a5277b" />
<img width="247" height="234" alt="image" src="https://github.com/user-attachments/assets/86f89adf-d37e-4a35-8c12-431c2703edcd" />

* This will be the file containing our usernames and passwords for our bruteforcing attack

# Step 9: Adding usernames and passwords to our created text files
* Open the user.txt and create up to 10 usernames for the last username it will be the true username of our attacking machine
* You are free to create your own usernames it may be 1, 2 or 5, it is up to you and the usernames you create are your own choices, same as the pass.txt
* For the last username "user.txt" it should be the correct username for this
<img width="644" height="513" alt="image" src="https://github.com/user-attachments/assets/ab025461-ed94-47a8-a895-04054af20909" />


* Same goes for the password "pass.txt" for the last password
<img width="640" height="516" alt="image" src="https://github.com/user-attachments/assets/88db3c3c-f3d3-4797-92c3-aa8ac7583c5d" />





# Step 10: Enabling SSH Service in Kali-Linux
* Input this command on kali-linux, if the ssh service is not yet activated

```bash
sudo systemctl status ssh
```

<img width="629" height="374" alt="image" src="https://github.com/user-attachments/assets/6d6a0489-2baf-40e6-8255-2676561f2859" />

* If not yet activated, input the command below:

```bash
sudo systemctl enable --now ssh
```

* Then re-check if it is activated by using the command:

```bash
sudo systemctl status ssh
```

* It should then receive an activation from the command
<img width="773" height="442" alt="image" src="https://github.com/user-attachments/assets/e7d7d0f2-f9c1-449f-b8d3-053d0c9cb10d" />


# Step 11: Opening ELK-STACK for Blue-Team Logs 
* Under the File Button, Click the Open button
<img width="1135" height="490" alt="image" src="https://github.com/user-attachments/assets/86f26c5c-357f-4553-a494-62bf66868e61" />

<hr>

* Under _RivanVMs folder on D: Drive or C: Drive, Find the ELK-OTRS.V1 or ELK-OTRS.v2 either way its fine, open the .vmx file
* If it is not yet extracted we need to extract it to get the .vmx file
* Under _RivanVMs folder on D: Drive or C: Drive, Find the ELK-OTRS.V1 or ELK-OTRS.v2 either way its fine
* then right click on the folder, then select winrar or any other extractor and click extract to*
<img width="687" height="199" alt="image" src="https://github.com/user-attachments/assets/5ee97301-7222-4acc-a5dd-39d5f54ed735" />
<img width="302" height="271" alt="image" src="https://github.com/user-attachments/assets/1a065f4d-e022-4c6f-bdb2-e4b94908a815" />

* Next is opening the .vmx file, double click the .vmx file to open it on VMware
<img width="627" height="45" alt="image" src="https://github.com/user-attachments/assets/12cf9883-6ea6-47a0-a669-a833a8bdc47f" />


<img width="616" height="283" alt="image" src="https://github.com/user-attachments/assets/3824283a-a102-4e6c-befe-f5c0138ba1a3" />

# Step 11: Powering ELK-Stack
* Click Power on this virtual machine, don't forget to check if the Network adapter is set to "NAT"
* If there is a pop-up if the virtual machine has been moved or copied just click "I copied it"
<img width="590" height="480" alt="image" src="https://github.com/user-attachments/assets/6bd0bc9a-b726-48e0-b52d-8232339f1105" />

<img width="378" height="208" alt="image" src="https://github.com/user-attachments/assets/c0ae620e-f575-47df-92ca-adc191eadded" />

* Next is logging in on the ELK-STACK, the username and password is root:C1sc0123
<img width="656" height="338" alt="image" src="https://github.com/user-attachments/assets/21e2398c-e292-463b-9304-f075cba9cbdc" />


# Step 12: Accessing CLI of ELK-STACK (Rocky Linux)
* Type the command to show the list of ipv4 addressses, and remember the et0 to connect it to securecrt
```bash
ip -4 addr
``` 
<img width="467" height="160" alt="image" src="https://github.com/user-attachments/assets/95e0b099-1a4e-47c8-bfb7-38d69df393bb" />

* Click kidlat, and input the ip address of the given ip on ELK-STACK (Rocky Linux), then click Connect
<img width="1258" height="671" alt="image" src="https://github.com/user-attachments/assets/dd15980b-93ee-4f93-9ac6-ade0571d727c" />


* The username and password is root:C1sc0123
<img width="370" height="191" alt="image" src="https://github.com/user-attachments/assets/d8fc6234-2b26-43b4-8fee-6250703b1a2b" />

<img width="687" height="155" alt="image" src="https://github.com/user-attachments/assets/ce478237-ced4-4308-93da-9f89686189dd" />


# Step 13: Configuring ELK-Stack via Filebeat
* We have to configure for the logs to be pushed through on the ELK-Stack, below is the step by step configuration
* 1st we need to check is rsyslog is running, on securecrt paste this command:
```bash
sudo systemctl status rsyslog
```
<img width="729" height="209" alt="image" src="https://github.com/user-attachments/assets/ca631c77-02a1-4be1-b65c-38c26ab429b4" />

* Next step is configuring filebeat.yml, because we need to enable the logs and add the logs location to see the current messages of logs, after pasting the command press enter
```bash
sudo nano /etc/filebeat/filebeat.yml
```
<img width="486" height="43" alt="image" src="https://github.com/user-attachments/assets/0d985aed-96ff-4940-8a67-f77883b10c2e" />

* Enable the filestream by using the navigation arrow keys, and add the following to the /var/logs, to save it Ctrl+S and Ctrl+X to exit.
* see image below:
<img width="1195" height="378" alt="image" src="https://github.com/user-attachments/assets/15b76211-6749-41f6-a7d7-0c9237ef31cd" />


* Then reload the system filebeat to update the configurations
```bash
sudo systemctl restart filebeat
```
<img width="436" height="41" alt="image" src="https://github.com/user-attachments/assets/35651bee-fa33-4127-9b7b-e9021431ce78" />

# Step 14: Opening ELK-Stack

* On the given IP Address of Rocky Linux, type on the browser:

```bash
http://(IP of Rocky Linux):5601
```
* The credentials for this is elastic:C1sc0123, then click Login
<img width="1494" height="700" alt="image" src="https://github.com/user-attachments/assets/a2262407-b2f0-4cdc-a829-2f7c2cb1336c" />
<img width="675" height="535" alt="image" src="https://github.com/user-attachments/assets/100c838c-7a71-4306-b456-f8bff704bf54" />
<img width="1895" height="811" alt="image" src="https://github.com/user-attachments/assets/705d79ed-a281-4e3b-b38a-2de4d0e1ad65" />

* Next is opening the Logs for incoming alerts, Go to the ☰ Hamburger icon, then click Discover
<img width="258" height="305" alt="image" src="https://github.com/user-attachments/assets/dca6591e-b181-460a-a395-321663279a6f" />
<img width="1915" height="860" alt="image" src="https://github.com/user-attachments/assets/934618f7-b50f-4c24-bed5-b16ee8589334" />

* Many Logs will appear, because we added another file directory for the ELK-Stack to save it, but we need to see the brute force of logging in and banning of IP Address later on.

# Step 15: Configuring MSFConsole
* Going back on Kali-Linux 2 Terminals must be opened, 1 is MSFConsole(Metasploit) and the other is using for ping and ssh login

<img width="1273" height="467" alt="image" src="https://github.com/user-attachments/assets/724d5a63-fd07-461f-9393-506801c2e13a" />

* Make sure that the attacking VM is reachable and pingable, that way we can access the ssh auxiliary of the metasploit
<img width="1274" height="765" alt="image" src="https://github.com/user-attachments/assets/ae376dcc-251b-40d6-820e-1906943d3f18" />

* On metasploit search for ssh_login
```bash
search ssh_login
```

<img width="742" height="301" alt="image" src="https://github.com/user-attachments/assets/4a721b67-1e40-4241-ae4c-3db1238ad068" />

* We will be using the index 0 of the ssh_login auxiliary, to do this use the command:
```bash
use 0
```

<img width="389" height="53" alt="image" src="https://github.com/user-attachments/assets/82bf8acd-eaf0-4539-a51d-fef931c52ec9" />


* Followed by the command "show options" to show what we can configure on the axiliary ssh_login
```bash
show options
```

<img width="715" height="659" alt="image" src="https://github.com/user-attachments/assets/e2146a1e-d9fb-4520-86a5-8aa935b70da1" />

* Now we need to Configure the settings of the auxiliary ssh_login
* 1st set the rhosts to the machine that we need to attack, "Rocky Linux IP Address"
```bash
set rhosts (Rocky Linux IP Address)
```
<img width="516" height="36" alt="image" src="https://github.com/user-attachments/assets/b5a5fc30-b778-4702-a0b5-a24f1cce0fd3" />

* 2nd is setting the user_file and pass_file, the one that we created text files on desktop
```bash
set user_file /home/kali/Desktop/user.txt
```
<img width="667" height="36" alt="image" src="https://github.com/user-attachments/assets/247ed947-c135-49af-b7f8-60e81cb52bea" />

* Same goes for the pass_file
```bash
set pass_file /home/kali/Desktop/pass.txt
```
<img width="704" height="38" alt="image" src="https://github.com/user-attachments/assets/4e3abb42-470e-4e26-8e18-0e56b340d298" />

* 3rd is settings the stop_on_success, so that if the exploitation had been succeeded it will stop and not continue to exploit
```bash
set stop_on_success true
```
<img width="561" height="35" alt="image" src="https://github.com/user-attachments/assets/f34b9c0f-7b43-4f0e-bfd4-a6afdeafd191" />

* 4th is settings the verbose to true, so we can see the failed and success process
```bash
set verbose true
```
<img width="497" height="31" alt="image" src="https://github.com/user-attachments/assets/9accf103-50fe-4fb4-8618-986e09cd7168" />

* 5th in configuring is checking again the options to check wether we inputted is correct, and if wrong we need to re-input the wrong input.
```bash
show options
```
<img width="720" height="700" alt="image" src="https://github.com/user-attachments/assets/ae101db2-3921-44fc-b2d0-47d3aabe4874" />


* Last setting, if all the settings is correct run the exploitation by running the command:
```bash
exploit
```
<img width="512" height="166" alt="image" src="https://github.com/user-attachments/assets/882ec10a-f1fe-45d2-91f0-ad97460852ae" />

# Step 16: Checking Logs on ELK-Stack
* On Discover search for:
```bash
message: "failed password"
```
* This means that someone is trying to access the system and trying to brute-force it, as blue-team now, we need to prevent this and block access if needed.
* 1st we need to demonstrate how is it going to succeed, wait for the verbose to finish from there we will see a success log that brute-force is succeeded and also on the ELK-Logs
* Another thing is don't stop the ping request of the attacking machine so that we will see if the you can succeed in blocking the icmp request and ssh brute-force login
<img width="1588" height="791" alt="image" src="https://github.com/user-attachments/assets/3b9e107f-95b9-4b18-abf9-ed15398de5b1" />


* There is a success happened on the procedure of brute-forcing the system, we need to prevent this, as blue team we need to prevent this from happening again
<img width="1482" height="735" alt="image" src="https://github.com/user-attachments/assets/e5247f35-8744-429d-893e-4b64c9e34833" />

* On Elk-Stack, to show the accepted password just type:
```bash
message: "Accepted"
```
<img width="1579" height="729" alt="image" src="https://github.com/user-attachments/assets/688e9103-db32-434a-b9f0-157c8143af01" />


# Step 17: Banning IP Address if Brute-Force happens
* To prevent this we need to simulate how prevention works, 1st we need to install fail2ban, Fail2Ban is an open-source intrusion prevention framework for Linux systems that automatically protects servers from brute-force and other automated attacks by monitoring system log files.
* Install it on the server (Rocky Linux) on SecureCRT, by using the command below:
```bash
sudo dnf -y install fail2ban
```
<img width="839" height="401" alt="image" src="https://github.com/user-attachments/assets/fbfe45f3-2469-41aa-92f0-49b824f639ea" />

* And enable the service using the command below:
```bash
sudo systemctl enable --now fail2ban
```
<img width="994" height="55" alt="image" src="https://github.com/user-attachments/assets/e6125d2a-124a-4e93-8ec6-e3f5dcaf57f8" />

* jail doesn't exist yet in Fail2Ban, we need to check the Existing Jails
```bash
fail2ban-client status
```
<img width="383" height="62" alt="image" src="https://github.com/user-attachments/assets/eb9bd4aa-95cd-4448-834f-be1aeda30739" />

```bash
fail2ban-client status sshd
```
<img width="656" height="68" alt="image" src="https://github.com/user-attachments/assets/0da955fc-10b3-4a08-9a00-2540ebe01023" />

* This means that it has no configurations yet, we need to activate it, below are the steps:
* Create Your First Real Config, This is the real fix. Enter the command below and press enter
```bash
sudo nano /etc/fail2ban/jail.local
```
<img width="474" height="27" alt="image" src="https://github.com/user-attachments/assets/b71d2998-2f87-4a12-b87b-770684250c2d" />

* Enter these commands, by copying and paste for easy access
* These commands have the maximum of 5 attempts of brute forcing after that, the server will automatically ban the ip address of the one who is doing the brute-force attack, after copying and pasting Ctrl+S to save and Ctrl+X to exit.
```bash
[sshd]

enabled = true
port = ssh
logpath = /var/log/secure
maxretry = 5
bantime = 300
findtime = 60
action = firewallcmd-allports
```
<img width="1229" height="641" alt="image" src="https://github.com/user-attachments/assets/ea589d22-1b35-4f69-897a-f1694b8407e6" />

* Then we need to restart the service for fail2ban
```bash
sudo systemctl restart fail2ban
```
<img width="482" height="48" alt="image" src="https://github.com/user-attachments/assets/265e0817-fb7d-4f52-9595-1ae2ed101065" />


# Step 17: Redoing Brute-Force Attack
* After doing the fail2ban procedure it will then send logs and send alert if the brute force attack has been done 5 or more times, the server will automatically ban the IP Address of the attacker and also ban the icmp request.
* On Kali-Linux re-run Exploit to see the changes it made.
* By running exploit again, we noticed the system server automatically closed the connection and banned the IP Address.
<img width="1458" height="227" alt="image" src="https://github.com/user-attachments/assets/fb383d09-8d17-457d-a1c1-5097e83047a4" />

# Step 18: Checking Logs on ELK-Stack and on fail2ban
* On the GUI of ELK-Stack, we can then limit the message by using the word:
* From here we will see that the server banned the attacker from using brute-force and icmp request or ping
```bash
ban
```
<img width="1587" height="738" alt="image" src="https://github.com/user-attachments/assets/efd51c42-bff4-40d6-9ec1-6beff6e46b85" />
<img width="1460" height="231" alt="image" src="https://github.com/user-attachments/assets/9b5bed62-26f1-42a7-b9a6-9936c816dd1b" />

* Lastly to check the banned ip on fail2ban, use this command:
* From here we see the fail2ban lists of IP Addresses
```bash
fail2ban-client status sshd
```
<img width="747" height="160" alt="image" src="https://github.com/user-attachments/assets/bb882475-81c5-4b0b-b126-3a18e87d99e1" />

* To unban an IP Address, do this command:
```bash
sudo fail2ban-client set sshd unbanip "attacker ip address"
```

<hr>
<hr>

* You Just Simulated A Red-Team Attacker, and Blue-Team Attacker all in one, only just you.
![360_F_1180235355_hzyweFZmPn7qax4hpfjKsDK9nAx7nH4L](https://github.com/user-attachments/assets/8ba0f7ef-636e-431f-b07a-9f4bb572eb7e)




