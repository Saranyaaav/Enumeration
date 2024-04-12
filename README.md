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
![Screenshot 2024-04-12 083110](https://github.com/Saranyaaav/Enumeration/assets/144870813/614666c9-cd8b-4d6f-ad05-91eba5257b1c)

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
![Screenshot 2024-04-12 083253](https://github.com/Saranyaaav/Enumeration/assets/144870813/ed5da52b-86ca-4354-8b4b-2d4e0443c381)



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
![Screenshot 2024-04-12 083502](https://github.com/Saranyaaav/Enumeration/assets/144870813/7252f164-0402-4871-afa5-6e843c3c46bc)


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![Screenshot 2024-04-12 083935](https://github.com/Saranyaaav/Enumeration/assets/144870813/bd3eab1f-c2eb-49d9-b910-d4e6e99884bd)

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
![Screenshot 2024-04-12 084156](https://github.com/Saranyaaav/Enumeration/assets/144870813/d3b77647-ead9-4fa3-bb06-935ff0953115)

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
![Screenshot 2024-04-12 084407](https://github.com/Saranyaaav/Enumeration/assets/144870813/39942274-2abe-4b28-ad60-f5cd9f418f86)

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.
![Screenshot 2024-04-12 084535](https://github.com/Saranyaaav/Enumeration/assets/144870813/6b97ea17-d79f-4067-8e73-d6d2331c3442)

 
# DNS Enumeration


## DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:
![Screenshot_2024-04-12_09_18_29](https://github.com/Saranyaaav/Enumeration/assets/144870813/9193656a-d1e7-4a94-869a-83cb930d8910)
![Screenshot_2024-04-12_09_19_29](https://github.com/Saranyaaav/Enumeration/assets/144870813/e53071fe-7909-4084-8b61-4bd60072d2ba)

## Dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
## OUTPUT:
![Screenshot_2024-04-12_09_18_59](https://github.com/Saranyaaav/Enumeration/assets/144870813/202e2a3d-8001-46ed-8d50-d350f03dc431)
![Screenshot_2024-04-12_09_19_11](https://github.com/Saranyaaav/Enumeration/assets/144870813/ec35cc04-0bde-4da6-8217-9f6ce3ea602c)

## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
## OUTPUT:
![Screenshot_2024-04-12_11_04_45](https://github.com/Saranyaaav/Enumeration/assets/144870813/aaa7ef2b-8658-4856-bc6a-9d31743c30c3)


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
## OUTPUT:
![Screenshot_2024-04-12_10_38_24](https://github.com/Saranyaaav/Enumeration/assets/144870813/7ba9e846-7f52-498a-807d-7b4f065fc018)

![Screenshot_2024-04-12_10_38_19](https://github.com/Saranyaaav/Enumeration/assets/144870813/36c52218-d449-43ec-a7c0-e4b3606a697d)


select any username in the first column of the above file and check the same
## OUTPUT:

![Screenshot_2024-04-12_09_27_46](https://github.com/Saranyaaav/Enumeration/assets/144870813/227c64ff-f614-4842-b7e4-8df621e3439a)

# Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
## Output
![Screenshot_2024-04-12_10_20_09](https://github.com/Saranyaaav/Enumeration/assets/144870813/35413791-1d49-4082-a629-64a34b2cb16d)
## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:

![Screenshot_2024-04-12_09_53_52](https://github.com/Saranyaaav/Enumeration/assets/144870813/df690442-3e4d-4cb3-94dd-ab4932a7e25b)


## RESULT:
___
The Google hacking keywords and enumeration tools were identified and executed successfully
___

