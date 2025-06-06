---
layout: post
title:  "Yummy Recipes: Apply OS Hardening Techniques"
date:   2025-05-28
categories: portfolio security
---

# Scenario

You are a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A former employee has decided to lure users to a fake website with malware.

The former employee/ hacker executed a brute force attack to gain access to the web host. They repeatedly entered several known default passwords for the administrative account until they correctly guessed the right one. After they obtained the login credentials, they were able to access the admin panel and change the website’s source code. They embedded a javascript function in the source code that prompted visitors to download and run a file upon visiting the website. After embedding the malware, the hacker changed the password to the administrative account. When customers download the file, they are redirected to a fake version of the website that contains the malware.

Several hours after the attack, multiple customers emailed yummyrecipesforme’s helpdesk. They complained that the company’s website had prompted them to download a file to access free recipes. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly.

In response to this incident, the website owner tries to log in to the admin panel but is unable to, so they reach out to the website hosting provider. You and other cybersecurity analysts are tasked with investigating this security event.

To address the incident, you create a sandbox environment to observe the suspicious website behavior. You run the network protocol analyzer tcpdump, then type in the URL for the website, yummyrecipesforme.com. As soon as the website loads, you are prompted to download an executable file to update your browser. You accept the download and allow the file to run. You then observe that your browser redirects you to a different URL, greatrecipesforme.com, which contains the malware.

The logs show the following process:

The browser initiates a DNS request: It requests the IP address of the yummyrecipesforme.com URL from the DNS server.

The DNS replies with the correct IP address.

The browser initiates an HTTP request: It requests the yummyrecipesforme.com webpage using the IP address sent by the DNS server.

The browser initiates the download of the malware.

The browser initiates a DNS request for greatrecipesforme.com.

The DNS server responds with the IP address for greatrecipesforme.com.

The browser initiates an HTTP request to the IP address for greatrecipesforme.com.

A senior analyst confirms that the website was compromised. The analyst checks the source code for the website. They notice that javascript code had been added to prompt website visitors to download an executable file. Analysis of the downloaded file found a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com.

The cybersecurity team reports that the web server was impacted by a brute force attack. The disgruntled hacker was able to guess the password easily because the admin password was still set to the default password. Additionally, there were no controls in place to prevent a brute force attack.

Your job is to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website.  You should also recommend a security action to take to prevent brute force attacks in the future.

# Security Incident Report

## Section 1: Identify the network protocol involved in the incident

We know that the protocol involved is the HTTP (Hypertext Transfer Protocol) since that protocol takes care of the website communication. Also, the tcpdump traffic log shows that the affected port is the port for HTTP, confirming our assumptions. The log also shows that the HTTP protocol is being used to push the malware file to the users computers.

## Section 2: Document the incident

After receiving reports from the clients, the IT team started to run tests on a sandbox environment. Running the network protocol analyzer **tcpdump**, the IT team navigated to the URL `yummyrecipesforme.com`. As soon as the website loaded, it promted to download an executable file to update the browser. After finishing the download, the browser was redirected to the URL `greatrecipesforme.com`.

The tcpdump log showed that at first the browser was correctly directioned to the IP address for `yummyrecipesforme.com`. Then the server pushed the executable download. Afterwards the browser was redirected to `greatrecipesforme.com`.

A senior analyst confirms that the website was compromised, and that the source code for the website was modified.

## Section 3: Recommend one remediation for brute force attacks

It is recommended to implement a Strong Password Policy, including more frequent password changes for the higher the privileges a role has. It is encouraged to enforce two-factor authentication (2FA) to avoid brute force attacks in the future.