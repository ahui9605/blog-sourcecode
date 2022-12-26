---
title: MS Server Test1
date: March 5, 2022
tags:
  - Exams
  - Code
categories: MS Server

#阅读模式，右下角开启
readmode: true

#封面
cover: https://partner.microsoft.com/-/media/mssc/mpn/partner/solutions/images/featurecontent-3-column-_500x280_windows_server.ashx?h=280&iar=0&w=500&la=en&hash=8DD80B877119E40C52E4659686958A37

#版权
copyright_author: Zehui Liu
copyright_url: https://ahui9605.github.io/

description: MS Server test1 answers
---

### MAIM

**1. A windows server uses an IP address 36.128.22.234. What is the socket address for the machine’s web server when it allows Secure HTTP connections?**
The socket is 36.128.22.234:443 where 36.128.22.234 is the IP address and the 443 is the HTTPS port" blue

**2. Which of the following is a private IP address?**

- 197.28.112.256
- 172.22.265.12
- 147.123.18.28
- {% label "10.1.12.213" blue %}

**3. What is the main purpose of Dynamic Host Control Protocol (DHCP) on a server? (Explain in your own words giving an example you see when starting and stopping your Google VM. If you copy-paste answers from generic google search no credit is given)**

These features can be added to Microsoft Windows Server through the server roles. On the server roles window, an option shows DHCP Server; according to the description, the aim of using the DHCP is to allow the user to configure, maintain, and distribute temporary IP numbers and other client-side information."

**4. What is the output of following Power Shell script? Run line by line in Power Shell command line window (NOT Power Shell ISE) and attach a screenshot.**

{% codeblock lang:POWERSHELL %}
cd c:\users\<yourname>\desktop # should show like C:\Users\danturthi\desktop>
new-Item abcd.txt
Add-Content abcd.txt “This is the first line”
Add-Content abcd.txt -value(get-content abcd.txt)
write-output “The file contents are:”
{% endcodeblock %}

**Answer this question - Which of the above commands is unnecessary/Superfluous (can be completely removed) in this particular example to achieve the same output?**

![](/images/MS/MS-4.png "I remove “Add-Content abcd.txt -value(get-content abcd.txt)” because it shows duplicated content in the powershell which is redundant and unnecessary.")

**5. In the windows server manager, you want to see the hard disk allocation and the available disk partitions or space. What options do you pick from Windows server manager window? Produce a screenshot on your VM that shows the disks and paste it here.**

![](/images/MS/MS-5.png "Open the Server Manager application, move the pointer to the left sidebar, and look for the File and Storage Services option. Then click the Volumes, available disk partitions and spaces will be display at the center of the screen.")

**6. When we do a scan for Best Practices Analyzer (BPA) on Windows Server 2019, what does it indicate for each role configuration?**

- A. If the role configuration falls through Microsoft’s control lists
- B. Whether the role configuration violates any existing practices
- {% label "C. If the role configuration meets Microsoft’s minimum guidelines" blue %}
- D. Whether firewall is actually working on the role configuration

**7. A programmer writes code - that is supposed to use a system account, but uses his own account (username and password) to test an application on a development machine. When all development and testing goes well, he transfers the code without any changes to you, the System Administrator (SA). When you deploy the code on production server, the code fails to run and says “incorrect username and password.” As the SA what do you think is the problem and how/what would you advise the programmer to fix the application?**

Before running a test on a production server, applications must modify their username and settings. Even the developer was able to successfully execute the applications on his development PC.

**8. Copy the following code to Power Shell ISE into file okay.ps1, save it and run it. Put your name below for correct path for your VM and Take a screen shot and enclose results of the script here and answer the following questions**

{% codeblock lang:POWERSHELL %}
cd c:\users\<yourname>\desktop # should be like C:\Users\danturthi\desktop>
Add-Content myFile.txt "`nName `tQ#1 `tT#1 `tGrade"
Add-Content myFile.txt "`nDavid `t45 `t110 `t155"
Add-Content myFile.txt "`nMelissa `t40 `t120 `t160"
Add-Content myFile.txt "`nRick `t50 `t90 `t140"
Get-Content myFile.txt | select-string 'a'| write-output
{% endcodeblock %}

![](/images/MS/MS-8.png)

- **(i) Explain what the “ select-string ‘a’ “ is doing**
  select-string ‘a’ (Select all the string values that included the letter ”a” from the file named “myFile.txt”) |write-output (output the selected string values and display on the screen from the powershell)

- **(ii) What are the characters “ `t “ and “ `n “ doing in the power shell script?**
  “`t“ means horizontal tab and “`n” means make a new line.

- **(iii) What happens if you remove all the “ `n “ characters from power shell script?**
  Powershell does not add any new lines to the output.

![](/images/MS/MS-8_2.png)

{% note modern warning%}
NOTE: The character before “n” and “t” is the backtick (next to numeric 1)
{% endnote %}

**9. On VM you open the command prompt in Power Shell window and execute the following command (If IIS is not installed, go to control panel -> programs and features and -> install Internet Information Server)**

{% codeblock lang:POWERSHELL %}
get-nettcpconnection -Localport 56
and you notice you are getting an error. Replace the port 56 with 80 and run again.
Now run this command: netstat -an | select-string 80
{% endcodeblock %}

**What do you conclude from the results of these three commands about ports 56 and 80? (Attach a screen shot)**

After installed the IIS in the VM, I am unable to get the TCP connection and view its property when I attempt the connection of localport 56 because this port could not be found. However, I am able to see the tcp connection of port 80, and its status is listening, also some established tcp connections.

![](/images/MS/MS-9.png)

**10. Stateful Packet Inspection (SPI) of a firewall is used for examining packets as they move in and out of a network.**
**What is the main focus of SPI?**
SPI mainly focused on connections

**What are rules SPI implements for internal and external connections?**
Internally connection allow by default and externally connection prohibit by default.

11. From the VM, choose google SDK command line interpreter and execute the following commands:

{% codeblock lang:CMD %}
gsutil du c:
gsutil du gs://<your bucketname>
gsutil du
{% endcodeblock %}

**Take a screen shot of the results (individually or together)and explain what it is displaying. NOTE: These commands may not work on Power Shell or DOS window**

![](/images/MS/MS-11.png)

**12. What three kinds of rules can you set up with Windows Defender Firewall on the Windows Server 2019 (Google Virtual Machine)?**

- (1) Inbound Rules
- (2) Outbound Rules
- (3) Connection Security Rules

**13. Open Google VM server in remote desktop, choose run and enter the following – Sigverif in the run window. When it shows the actual application, run it and click “Start” on the application. When it is finished, attach the resulting log file contents to this test (add another page, if required)**

![](/images/MS/MS-13.png "Here is the screenshot of the log file after finishing the scan.")

**14. When a firewall examines packets as a part of stateful packet inspection logic, what are the two main categories a packet state can fall into?**

- A. Packets opening connections and packets closing connections for data move
- B. Packets trying to send data and packets trying to receive data from connections
- {% label "C. Packets trying to open connections and packets not trying to open connections" blue %}
- {% label "D. Packets that are static with same IP and packets that are dynamic with variable IP" blue %}

**15. Your Network/Server has a border firewall to block/deny any suspicious attack packets. Besides blocking the packets, what must the firewall do for the system administrator?**

Firewall not just only process the regular check to block packages, but also can drop and update logs, caution the SA if there is any suspicious action appear

### BONUS

**16. Your firewall has a 276 rules you created in addition to the default rule to examine and allow or deny packets. As a System Administrator you are given the job of arranging these access control rules in a numerical list known as Access Control List (ACL).**

**A. Which rule will be your first rule and which rule will be your last rule in the ACL? (Just mention how you pick the first rule and last rule and on what criteria).**
The first rule will be creating a set of rules that the firewall may use to monitor various packages as the priority. The default rule usually will be the last execution in the rules list.

**B. What happens if you swap (exchange) the first rule to the last?**
Swapping the rule to the default rule first may not be a smart idea since if the default rule is successful, the rest of the rules will not be executed.
