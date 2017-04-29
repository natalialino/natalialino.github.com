Computer Architecture and Systems - Project and Learning Journal
Student Natalia Barreto Lino - 17325

Introduction

The aim of this project was to successfully install and fully configure a virtual machine hosting a LAMP stack and to demonstrate a web application functioning on it. The three main stages can be listed as follows:
The initial configuration of the virtual machine and installation of the operating system (Linux Ubuntu)
Installation and testing of the Apache web server, MySQL database and php processing module.
Installation and testing of the CMS and modification of the hosted content. Word 
This report will cover these stages in a step-by-step manner with a special focus on the learning process involved.

Explanation of Virtualization and VM VirtualBox. 
Concept of Virtualisation explained. 

It can be defined as the computational solutions that apply to the execution of several operating systems and their respective software from a single machine. The difference is that these machines are virtual: in practice, the results are just like any other computer, but only logically, not physically.

Each virtual machine translates to a complete computing environment: practically all the features of your operating system can be used, you can connect them in a network, and you can install applications and so on. 

Some advantages
- Test environment: it is possible to evaluate a new system or an update before actually implementing it, significantly reducing the risks inherent in such procedures;

- Security and reliability: Because each virtual machine works independently of others, a problem that arises in one of them, such as security vulnerability, will not affect the others;

- Centralized management: depending on the virtualization solution used, it is easier to monitor the services running, since its management is done in a centralized way;

How does virtualization work?
A virtualization solution consists essentially of two "protagonists": the host and the guest. The host being the operating system that it runs by a physical machine. The guest, in turn, is the virtualized system that must be executed by the host. Virtualization occurs when these two elements exist.

Virtual BOX
VirtualBox is an Oracle virtualization program that allows you to install and run different operating systems on a single computer without complications. With it, the user can run Linux within Windows 7, Windows within the Mac, Mac inside Windows and even all supported systems within one. You can also install Android on other machines.

Configuration and Deployment of the Virtual Machine 
The application allows you to make various adjustments to individual virtual machine configuration. What I have done in class following the steps available on Moddle :

1.	Download Ubuntu Server OS 16.04. I used a copy from the teacher. We will use Ubuntu Server OS 16.04.
2.	 I created a Virtual machine to install our guest Operating System. Using VM VirtualBox create a machine for hosting our 32 Bit Ubuntu Linux server selecting the size and type of the drive. Configurations suggested on the project step: • Memory Size: 2048mb • Virtual Hard Disk: VDI, dynamically allocated, 20gb 
3.	 Install Ubuntu Server. After setup was configured I enter the hostname for my computer (Ubuntu). Username natalia1. 

What is a web server?
Web servers are responsible for storing and exchanging information with other machines. Because of this, at least two participants are involved in each exchange of information: one client, who requests information, and one server, who responds to those requests.

Each side also requires a specialized program to negotiate a data exchange. In the case of the client, a browser is used, such as Internet Explore or Firefox. On the server side though, how things are not so simple. There are several software options available, but they all have one task: negotiating data transfer between clients and servers via Hypertext Transfer Protocol (Http), or Web communications protocol. The software depends on the operating system chosen for the server.
Generally speaking, the web server is responsible for storing and exchanging information with other machines. Basically two participants are involved in information exchange: the users / clients (requestors) and the servers (attendants).

In summary, communication between the user and the server is given by the decomposition of the URL (web address) for the browser in several parts (domain name and page protocol). The DNS then translates the domain entered by the user into the IP address (numerical combination of the actual web site address) for the browser to determine which protocol to use (FTP, file transfer protocol, and http , Hypertext transfer protocol).

Given an example:  When the user types http://www.schoollinux.com, the browser requests the file from the server and waits for the response. The server responds after checking that the address exists and finds the required files, then executes the instructions and delivers the results. When it does not find, the server displays the error message (Error 404, usually).


APACHE 
HTTP Apache is a WEB server responsible for providing pages and all resources that can be accessed by the user. Sending e-mails, messages, online shopping and various other functions can be performed through Web servers as such as Apache.
It was created in 1995 by Rob McCool, an NCSA employee (National Center for Supercomputing Applications).The main idea was to supply the interpretation of Web programming languages, usually more used for PHP programmers. It is widely seen on the internet hosting servers that offer the Apache server its packages.

What is the Apache server for? 
Apache has the ability to read the program, and convert it by making the systems run in "user" mode, by turning everything that has been written into command lines into a visual form and interaction with system users. At first the Apache server existed only for UNIX platform, running on related operating systems, such as Linux and FreeBSD, currently exists also for Windows platform. The recommendation is that it be used on UNIX platform for the best performance.
Why use the Apache server?
 Firstly, because the apache server is extremely fast, the same is developed by several programmers because it is open source, with this, situations of several users are not corrected where it has several updates.
Advantages:
 Being used by around 80% of users worldwide, the system is considered the most reliable and stable to use, covering several options for the most varied situations and also it is a totally free open source system. 

Explanation of settings and configuration selected
 
In class:  Installing WEB APACHE and Deploying a LAMP stack on your Ubuntu Server:
A "LAMP" stack is a group of open source software that is typically installed together to enable a server to host dynamic websites and web apps. This term is actually an acronym which represents the Linux operating system, with the Apache web server. The site data is stored in a MySQL database, and dynamic content is processed by PHP.
We have already installed Ubuntu Server the second step is to install the APACHE Web Server.  
Follow bellow the steps given by the teacher. 

1.	Log into your VM (if updates are available you can install them with the sudo apt-get upgrade command). 
2.	Enter the command below to install the Apache Web Server: sudo apt-get install apache2 apache2-utils 
3.	We want to change our setting so the Apache2 web server will start up at system boot. To do this enter the systemctl enable command. Type the following: sudo systemctl enable apache2 
4.	We also want to start the service now by entering the command: sudo systemctl start apache2 
5.	Let’s check that our Apache server is up and running. First we will need to make sure that our network adapter settings make our VM visible from our host. We will need to shut down our VM and change the settings on our virtual network adapter. By default our adapter is configured as a Network Address Translation. We can set up port forwarding with our host to make it accessible from the host. These settings can be accessed through the Settings – Network – Advanced – Port Forwarding”
	
Installing the MySQL
Install MySQL MySQL is an open source Database program. It’s vital for many features of modern websites to maintain databases for purposes such as allowing users to login, saving any user generated input to the website e.g. posts on a forum etc. 
To install our MySQL database server run the following command: 
sudo apt-get install mysql-client mysql-server 


Reflection 
Verifying and testing the software for installation of the Virtual Machine the server/ web server. The teacher tried his best to accelerate the process; however, we had some delays in the first stage of the project installing the Ubuntu server. Another problem was the passwords and login for the Virtual machine. For future projects, I would recommend annotating login and password of all programs that it will be accessed. This information cannot be forgotten, it is not possible to recover a password and user login on the Virtual Box. Overall, it was a step by step project, fundamental for a first-year IT student.

Web Sites consulted 
http://www.hardware.com/comunity/virtual-machine/869168/
http://www.techtudo.com.br/tudo-sobre/virtualbox.html
https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04
https://www.infowester.com/virtualization.php
https://www.scribd.com/doc/62978470/What-it-is-and-what-is-for-Apache-server



