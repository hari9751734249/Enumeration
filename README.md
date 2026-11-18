# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

<img width="945" height="448" alt="image" src="https://github.com/user-attachments/assets/1110cfa1-87cf-4ccc-97a3-ff9e52ed7252" />


filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
<img width="956" height="449" alt="Screenshot 2026-11-05 154624" src="https://github.com/user-attachments/assets/da60821a-16d0-4ad5-97ca-56171256c851" />


intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
<img width="953" height="446" alt="image" src="https://github.com/user-attachments/assets/057b4f97-17fe-40ae-a8d5-57e858c11875" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
<img width="957" height="386" alt="image" src="https://github.com/user-attachments/assets/7d23f714-3881-4d9e-94f9-6abc50f56e3f" />

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
<img width="959" height="446" alt="image" src="https://github.com/user-attachments/assets/884b6f5d-32a7-4e59-9a0a-6f13fe3b1fca" />

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
<img width="947" height="446" alt="image" src="https://github.com/user-attachments/assets/eaa442c8-25f8-4c27-a65d-e2b04c9f886e" />

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com websit
<img width="940" height="440" alt="image" src="https://github.com/user-attachments/assets/9f1f17c3-8f39-4fed-9c27-0ff89e44d775" />

 
#DNS Enumeration

##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:

<img width="425" height="393" alt="image" src="https://github.com/user-attachments/assets/15bf253a-4901-4e8a-af2a-358e385eeff6" />







## dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
```
dig yahoo.com A
```
<img width="1059" height="708" alt="image" src="https://github.com/user-attachments/assets/08f4c937-5521-4e2f-8b07-bd321fdfe66a" />


Get the namservers (threaded).
```
dig yahoo.com NS
```
<img width="1920" height="892" alt="VirtualBox_Parrot Security 6 0_18_11_2026_08_44_41" src="https://github.com/user-attachments/assets/b53010a3-fc22-415c-b9bb-3d0b17edbde9" />


Get the MX record (threaded).
```
dig yahoo.com MX
```
<img width="434" height="354" alt="image" src="https://github.com/user-attachments/assets/4007f563-9adb-41ad-83b8-724326c7d7fc" />

Perform axfr queries on nameservers and get BIND versions(threaded).
```
dig @ns1.yahoo.com yahoo.com axfr
```
<img width="586" height="212" alt="image" src="https://github.com/user-attachments/assets/554083ed-9a78-4b09-ac37-56e5aad9d1b7" />


##DNS Enumeration using dnsenum:
```
dnsenum yahoo.com
```
<img width="524" height="393" alt="image" src="https://github.com/user-attachments/assets/539c1846-c71b-4dc9-b8e4-33030aa07529" />



## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same
## output
<img width="720" height="400" alt="VirtualBox_metasplot_18_11_2026_08_55_08" src="https://github.com/user-attachments/assets/2dcb25c5-5610-4253-84a8-0c72bb74b5f9" />

<img width="613" height="401" alt="image" src="https://github.com/user-attachments/assets/eb0a789e-2a34-458c-b40d-c67ff5734215" />





## Telnet for smtp enumeration

Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ## Output
 <img width="1753" height="897" alt="image" src="https://github.com/user-attachments/assets/8e8b80df-fab8-40e2-9391-fcce3eaf28a9" />

 
 
 


  
  

## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
<img width="2094" height="751" alt="image" src="https://github.com/user-attachments/assets/af8f9974-2e0e-49ae-a5db-8d8ff68bc32e" />



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

