<p align="center">
<img src="https://i.imgur.com/G9fOPue.png"/>
</p>


<h1>Implementing a Virtual Machine Using Microsoft Azure</h1>
Tutorial for creating and deploying a Windows 10 Virtual Machine (VM).<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)

- <h2>List of Prerequisites</h2>

- Microsoft Azure Active Subscription


<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/bfbfca8f-f77c-4204-8060-118a504a16a8)
<p>
Step 1: Navigate to "portal.azure.com/#home" to create a Resource Group. You can either select Resource Groups from the home screen or at the top of the page you can search Resource Groups and select it from there. This will house the resources we're going to create (ex: The Windows VM we're creating).
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/38f4bb16-d3f8-4ce0-8325-66635733413f)
<p>
Step 2: Click "Create" to create the Resource Group
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/0cea2614-59db-4382-bd5f-e47c49f1c6fc)
<p>
Step 3: Select what Subscription you want the Resource Group to go into if you have more than one Subscription but we only have one so we will choose "Azure Subscription 1". Next you will name your Resource Group and for this Demo we'll just name it "VM-LAB01". From there select what region you want the resources to be created. Also some resources are not available in every region. So for this project we're going to create our resources in "(US) East US". Then at the bottom of the page click "Review + Create".
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/4f50c343-7043-46a2-a5c9-edf7333846c0)
![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/3c5cfd62-2f18-4593-b4e9-58923b204ec5)
<p>
Step 4: Now that the Resource Group is created, we can begin creating our Virtual Machine (VM). From here you can either search Virtual Machines at the top of the page or you can go back to the Home page and select Virtual Machines from there. Click Create and select Azure virtual machine.  
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/90d0e4ff-c036-47d6-93a5-1c127af29ba7)
<p>
Step 5: Select the Resource Group we created (VM-LAB01). Name the VM whatever you like so I'm going to name mine (VM-1) just to keep it simple. Then select the same region that we put the Resource group in which was (US) East US. We're going to leave the Availability and Security type as the default settings.  For Image, since we're creating a Windows VM I'm going to select (Windows 10 Pro, version 22H2 - x64 Gen2)
</P>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/7f31a00a-0785-4e90-9dbe-fba93798ceb9)
![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/fe20dab8-b568-4acc-ac97-dd6f1aafc5a4)
<p>
Step 6: Next we will select the size for the VM which essentially determines the performance of the VM you're creating. Since we're just creating one VM we should be fine with selecting (Standard_DC2s_v3 - 2 vcpus, 16 GiB memory ($140.16/month). Choose a Username and Password (Username: labuser). (NOTE: Take note or remember what you choose because you will need it later on in the tutorial.) Check the Licensing box and click Next.  
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/9123dd49-2f01-47ee-9275-c27ed1a7e621)
<p>
Step 7: We're going to leave the Disks setttings as is. Click Next to Navigate to Networking.   
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/1d1cfac9-82cf-4713-adb5-2054f3ee25ec)
<p>
Step 8: This is where the Virtual Network and Subnet will be created automatically. The VM will have 2 IP Addresses, your Public IP Address which is accessible from the internet which will be used to connect to the VM later and the Subnet (10.0.0.4/24) which is the Private IP Address that will be used to communicate between another VM we'll create in the next Project. Click Review + Create. 
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/ec448d2a-decf-4f03-95e9-54bb9b2c3012)
<p>
Step 9: Once validation has passed. Click Create and we will wait while our VM is being deployed.    
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/8a53fb07-e842-45eb-a5de-65f092a0c020)
<p>
Step 10: This isn't necessarily a step but here you can see the Resources such as the VM, NIC, Network Security Groups and Public IP Addresse are being created within the Resource Group we created.  
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/9f07e785-bf27-46bc-9e24-f581c66af3ab)
<p>
Step 11: After deployment is complete, to navigate to your VM which is (VM1) you can click "Go to resource", type in virtual machines in the search bar or go to the home page in the portal and select virtual machines. 
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/8da439ad-a614-4406-a95c-ceea769fc784)
<p>
Step 12: Next we're going to login to our VM via Remote Desktop Connection. So what you want to do is click the Start menu and type in Remote and you should see (Remote Desktop Connection) and open the app so that we can connect to our VM. 
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/720509e5-0d00-48a2-b170-85af5760ba76)
![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/35651cc0-b5ec-41d8-b91d-348275055528)
<p>
Step 13: Now we're going to copy & paste our VM Public IP Address (48.216.212.118) then click connect.   
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/d4649056-d2dc-4d7f-aceb-1bbbc30c4ca9)
![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/cb6b9725-8207-42bf-8597-13ff134409d4)
<p>
Step 14: Select more choices and enter the Username (labuser) and Password that we created in Step 6.  Don't be alarmed when the second screen pop up after logging in, just select Yes to continue connecting to the VM. 
</p>
<br />

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/a370c6b7-6380-4534-984f-43eb133a649a)
<p>
Step 15: Honestly these privacy settings don't matter for tutorial purposes so we're just going to deselect all of the options and click Accept. 
</p>
<br /> 

![image](https://github.com/marcusjonesIT/configure-vm/assets/174873189/5c82539c-20d9-48d8-8578-6695b1b46e57)
<p>
The screen should look similar to this and we have now successfully deployed and connected to our Virtual Machine. From here we can do a variety of tasks such as test new operating systems, new applications or safely test new things without affecting our own computer. 
</p>
<br />
 























