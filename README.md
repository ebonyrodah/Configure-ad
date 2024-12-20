<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Prerequisites</h2>

### **1. Virtual Machines**
- **Windows Server 2022** After installation and configuration of the Active Directory Domain Services we will promote the server to a 
    Domain Controll
- **Windows 10** This will be our Client computer, we will use this to establish a connection with the server.
### **2. VNET**
- **Virtual Networks**: A properly configured Azure Virtual Network where both the domain controller (DC) and the client computer can communicate.
### **3. Network Configuration**
- **Static IP**: Assign a static private IP to the domain controller to ensure consistent communication.
- **DNS Configuration**: Configure the VNET settings on Client1 to use Domain Controller's private IP as the DNS server.
- **Ping**: We'll use this to check for connectivity.
### **4.Active Directory setup requirements**: 
- **Domain Name**: Setup a domain name for the Active Directory
- **Firewall Configuration**: Switch off the open ports for Active directory and domain joining.
- **Administrator Account**: Setup an administrator account with a password for setting up and managing the domain.
### **5. Powershell**:
-  To configure and manage settings programmatically.
### **6. Remote Desktop Connection**
- To log into client1 and the domain controller we'll use RDP.



<h2>Deployment and Configuration Steps</h2>
Below are some of the steps that were used to setup Active directory domain services and configure it.

---

## 1. Setup Domain Controller in Azure  
1. Create a **Resource Group**.
2. Create a **VNET**
3. Setup **Virtual Machine** for the Domain Controller.
-   setup the virtual machine name **`DomainControl`** select a region for it.
-   Create a resource : **`Activedirectory_lab1`**
-   Operating System: **` Windows server 2022 Datacenter`**
-   Username: **`Labuser`**
-   Password: **`Domainuser@1234`**
-   VNET :**`ADVNET`**
4. As you create the VM ensure you put it the same region as the resource group and Virtual Network.
  

<p>
<img src="https://i.imgur.com/iiuu38j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

---


## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---


## 3. Configure and connect the DomainControl
1. After the deployment of the Domaincontrol go to **>Network interface** **>IP configurations** click **>ipconfig1** then change it from dynamic to**>Static**
</p>
<br />

<p>
<img src="https://i.imgur.com/cPpnc1z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 4. Configure client1  
1. Go to Domaincontrol and copy its private IP address
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


---



## 2. Setup Client-1 in Azure  
1. Create the Client VM (Windows 10) named `Client-1`:  
   - **Username**: `labuser`  
   - **Password**: `Cyberlab123!`
2. Attach the Client VM to the **same region and Virtual Network** as `DC-1`. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVoOz5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
