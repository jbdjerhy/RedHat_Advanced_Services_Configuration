# RedHat_Advanced_Services_Configuration
This project aims to upgrade various aspects of the IT infrastructure efficiently. It covers the various commonly used server/client services. 
# IT Infrastructure Upgrade Project

## Project Overview

This IT project aims to enhance the existing IT infrastructure by implementing various improvements and configurations across multiple areas, including virtualization, system monitoring, iSCSI, NTP, LDAP, network services, DNS, web services, NFS, and SMB services. The project encompasses several phases, each focused on a specific aspect of infrastructure enhancement.

## Project Phases

#### Installing and Configuring Virtual Machines (VMs)
- Installed CentOS 8 Stream as the base operating system.
- Updated packages using sudo dnf update.
- Installed essential development tools and libraries.
- Took a snapshot of the updated base install.
- Resolved repository deprecation issues.
- Migrated to Rocky Linux using the migrate2rocky.sh script.
- Gathered system statistics using sysstat.

### Phase II: System Monitoring and Reporting

#### Creating System Reports with Sysstat
- Checked system logs in /var/log and analyzed the sa29 file.
- Utilized various sar options such as -d and -x.
- Used the userlog.sh script to create user-specific logs.
- Scheduled report generation with cron and monitored system performance.
  
![image1](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/231d0006-99dc-4258-ad0a-335a2a439031)

![image2](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/5667d292-2dee-4e30-a063-568575502d21)

![image3](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/ecec513d-c267-47a2-acc1-e2d62f100340)

![image4](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/41d4ed83-dec6-4ad2-b7cf-73bbbe434461)

### Phase III: iSCSI Target Configuration

#### Configuring iSCSI Target and Initiator
- Cloned rhhost1 to create rhhost2 as the target.
- Configured iSCSI target on rhhost1 using targetcli.
- Installed and configured the iSCSI initiator on rhhost2.
- Created an iSCSI backstore and LUNs.
- Implemented access control and authentication.
- Verified iSCSI target availability using netstat.
   - 
![image5](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/106b68ad-2134-4243-aef9-348d19be0926)

![image6](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/6e526822-d053-412a-803b-4b96f378d8c8)

![image7](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/fd73e9d2-f86b-46f7-a6c0-37206b2d80b6)

![image8](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/fe0658e6-9e0c-4adc-b0a8-208091051e10)

![image9](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/eea309c3-66c3-4155-87ef-0964d7280937)

![image10](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/a4fa6182-de38-4697-9379-0553c536a935)

![image11](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/f2000b1b-c62e-46a2-9ef5-c5b9271d2f9a)

### Phase IV: Network Time Protocol (NTP) Server Configuration

#### Setting up an NTP Server
- Checked the status of the Chrony service.
- Configured rhhost1 as an NTP time server and allowed requests from the local network.
- Opened the necessary firewall ports for NTP.
- Configured rhhost2 as an NTP client.
- Synchronized time with rhhost1 and verified synchronization.
  
![image12](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/a6d85bbf-927f-464f-9e33-e306417ce532)

![image13](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/1802df2b-3010-419f-ba3f-0f619417a815)


### Phase V: Authentication Services with LDAP

#### Implementing LDAP for Authentication
- Installed LDAP packages on rhhost1 and configured SELinux booleans.
- Started and enabled the LDAP server (slapd).
- Loaded LDIF files to set up LDAP directories and users.
- Configured LDAP client on rhhost2.
- Tested user information retrieval using getent passwd.
     
- ![image14](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/9456582a-26eb-45ac-bf69-d58c2a7f3f9d)
- 
![image15](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/201913ee-c64b-44e4-8c79-5b407910c3b0)

![image16](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/78ca69a5-10c5-4f83-bd92-cc448891e54c)

![image17](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/f5b66235-39d6-4866-95c0-ecf64af0fa6b)

![image18](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/5c283004-d152-47d6-8ff8-ef336721c16e)

![image19](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/9fe87191-947e-4fde-a8d6-321dab1b57af)

![image20](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/237fa9cf-0d9d-46e5-a57a-2ab668458a8e)


### Phase VI: Network Services Introduction

#### Introducing Network Services
- Installed network tools and utilities.
- Checked network interfaces, hostnames, and NetworkManager status.
- Configured interface bonding and teaming.
- Verified the status of bonded interfaces.
- Demonstrated the creation and removal of bonds and teams.
- Introduced basic firewall configuration and management.
     
![image21](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/53902bac-da53-4456-ae50-fd1fd243912e)

![image22](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/e8765f5a-f79b-4da7-9b33-54f63a5a23ba)

![image23](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/3a0141b6-67b4-42e0-a961-de3fd3b0ae07)

![image24](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/92d29e58-e01f-4043-9191-2bf1c92a669e)

![image25](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/6e303269-4597-4be2-af74-dbb9a9848d81)

![image26](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/c64ad0af-c44b-48df-8b22-a2142358f38d)

![image27](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/d10751f8-667e-4839-b1b3-9e3fb0aeb051)




### Phase VII: DNS Service Introduction (Setting up a Cache DNS)

#### Setting up a Cache DNS Server
- Installed and configured BIND (named) as a cache DNS server.
- Modified the configuration to allow DNS queries from any address.
- Disabled DNSSEC features for simplicity.
- Checked DNS configuration and firewall settings.
- Configured a DNS client on rhhost2 to use rhhost1 as a DNS resolver.
- 
![image28](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/42cabdf2-83d0-48e0-9653-057e797c3b61)


### Phase VIII: Web Services with Apache

#### Configuring Apache Web Services
- Installed Apache HTTP Server and related packages.
- Started and enabled the Apache service.
- Configured the firewall to allow HTTP traffic.
- Customized the default welcome page and verified the changes.
- Explored SSL configuration in /etc/httpd/conf.d/ssl.conf.
- Created and secured a virtual host with SSL support.
- Demonstrated SSL certificate creation and installation.
- Configured password-based authentication for a private website.
- 
![image29](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/845fc1f1-6ea9-48b6-88c4-287a7fb5c920)

![image30](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/7a7e293e-c126-4a7f-835f-87f742741f9c)

![image31](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/f1d279c6-5923-4a7f-a7ce-604a875fd7d5)

![image32](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/c4d749d0-2138-4253-a56d-f2fccdb11964)

![image33](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/58171bef-6038-4c19-a6df-c3ef95231a32)

![image34](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/a7af7938-a63a-427b-82dd-c9e71ac81675)

![image35](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/6cc11de9-4e71-44ff-8555-247c693e6c83)

![image36](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/ebc04868-6d47-49b7-944f-ee842ae7bf95)

![image37](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/7eef1968-2ce8-4ed5-b070-a2ea0bf8bac2)

![image38](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/1d88a5f4-2995-4677-a545-7987e49fa7d8)

![image39](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/187f1fdf-7748-49e2-86db-6869b19a412e)

![image40](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/afc56f44-8882-4b7c-a877-dccec779998e)


### Phase IX: NFS Services

#### Configuring NFS Services
- Installed NFS utilities on both hosts.
- Managed SELinux booleans for NFS.
- Created a directory for NFS sharing and set appropriate permissions.
- Exported NFS shares and tested NFS mounting on rhhost2.
- Demonstrated group collaboration with shared NFS directories.
  
![image41](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/20e1b829-6dc8-4c91-a494-28ad8751c82f)

![image42](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/acabd9f7-d3c4-4385-b23c-2b72ca77951f)

![image43](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/18fd107a-1a54-41f2-8956-b56412e7734e)

![image44](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/774d3f2b-498e-46aa-ad5c-2f38ca252dbf)

### Phase X: SMB Services (Samba)

#### Implementing SMB Services with Samba
- Installed Samba and related packages on both hosts.
- Checked existing SELinux booleans and adjusted them as needed.
- Configured Samba shares for both public and private access.
- Set up user accounts and passwords for Samba access.
- Tested Samba shares and access permissions.

![image45](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/6e057fe8-369b-45d7-a2b7-a2bc9ca50461)

![image46](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/af37cb5e-c6a1-4112-b9c7-2bae2a630b35)

![image47](https://github.com/jbdjerhy/RedHat_Advanced_Services_Configuration/assets/142699688/aa0d8a72-c37f-473c-a4d7-108403b7bf81)

























