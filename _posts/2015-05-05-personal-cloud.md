---
title: "Personal Cloud - A Silver Lining"
date: 2015-05-05 15:27:14 -0500
categories: private personal cloud 
badges:
 - type: info
   tag: info-badge 

---

# Personal Cloud - A Silver Lining    
### Into every life, a little rain must fall
Queue the Thunder Storms... and Action!    
> So, my computer crashed a few weeks ago, and initially, I lost "everything;" OS Drive and Parity drive in RAID, both dead. Most of us have experienced that tragic feeling at one time or another. I believe mine went something like.... OMG! What the?! No!!  
> Followed by a slew of Q*bert symbols as reality sunk in.  

After a lot of work scanning my drives and rebuilding the RAID with special tools ranging from other OSs to direct copiers, I recovered all but a few weeks of information.  

Like many, I know that several paid services are secure (if your credentials are) and reasonable. While I have no qualm storing information in the “ambiguous cloud,” I really prefer the ability to “see and touch” the places where I store more sensitive data for safe keeping.  

This prompted me to setup MY own cloud…  

---

### Private / Personal Cloud 
##### Cluster  
I took 3 old computers and wiped them clean. After reviewing several products, Proxmox seemed to fit my needs quite well. So, I installed Proxmox as a hypervisor, and clustered the computers together. BAM, instant, cheap high availability virtual cluster.  

##### Firewall  
Then, I reviewed a ton of different firewalls. While I wouldn’t necessarily call m0n0wall the “best,” I loved how small, quick, and easy to configure it was. Oh yeah, and I know BSD… I really liked a few of the Linux firewalls, but they were so bloated in comparison. So, I installed and configured m0n0wall.  

##### Ubuntu  
OS, OS, which OS? While I do love Windows, it’s definitely the furthest thing from my mind when I think light and quick. That coupled with my Ubuntu history made the decision easy. Linux it is.  

Install, configure, google, configure, google, reconfigure, google, google, head scratch, boggle, boggle, patch, install, patch, & run! Whew! When Company A decided to relieve company B of code, why couldn’t they just keep the same syntax?  

##### OwnCloud
Perhaps I should have researched the cloud solution a little more, but I’ve been dying for an excuse to setup OwnCloud for a while now. Therefore, “sudo apt-get install owncloud” and a little while later, I was logging in a configuring the admin account, groups, and users. If I’m going to make it, then why not let family use it too?  

##### FreeNAS
I built a NAS and connected it to the cluster.  

I redirected OwnCloud to pull from the NAS.  

And finally, l published the cloud through a domain that I own.  

### A Silver Lining  
Now I have my own cloud service that my family and I can backup our computers, phones and tablets to from anywhere, or access to store and retrieve data, pictures, etc...  

![img](https://media-exp1.licdn.com/dms/image/C5612AQGVmu4Z2E-JgQ/article-cover_image-shrink_423_752/0?e=1605139200&v=beta&t=DLBmHHervboOsUPIwCMMgHHtaF7FeZJsaw7f7D02sCo)  

---

#### Links:  
[Proxmox](https://www.proxmox.com/en "Proxmox")  
[Ubuntu](http://www.ubuntu.com/ "Ubuntu")  
[M0n0wall](http://m0n0.ch/wall/index.php "m0n0wall firewall")  
[FreeNAS](http://www.freenas.org/)  
[OwnCloud](https://owncloud.org/)  

