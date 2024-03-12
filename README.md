<h1>Configure Network Access in Azure using Cloud Shell</h1>

<h2>Description</h2>
This lab will create a Linux virtual machine in Azure using Azure CLI, and configure access to that virtual machine .
<br />

<h2>Environments Used </h2>

- <b>Microsoft Azure and Learn Sandbox</b>

<h2>Lab walk-through:</h2>

<p align="center">
<h4>Step 1</h4>
Get into the Azure Cloud Shell<br/>
<img src="https://i.imgur.com/0uUxgpc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
<h4>Step 2</h4>
From the Cloud Shell run the command to create a Linux VM<br/>
<img src="https://i.imgur.com/Hk9dV1g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h4>Step 3</h4> 
Run the command to configure Nginx on the VM<br/>
<img src="https://i.imgur.com/mvQN6p3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
<br />

<h4>Step 4: Access the web server</h4>
Enter the command to get your VM's IP address and store result as Bash variable.
<img src="https://i.imgur.com/nBUXmg6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Run curl command to download the homepage, After 5 seconds the connection will timeout, becaue VM was not accessible with the timeout period.
<img src="https://i.imgur.com/DIILfQN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Download your IP Address, and access it via a web browser. The connection will fail.
<img src="https://i.imgur.com/iVIp1MR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
<img src="https://i.imgur.com/ZMI7nP0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
<br />

<h4>Step 5: List Network secuity group rules</h4>
Run the command to list the network security groups that are associated with your VM, you will my-vmNSG.
<img src="https://i.imgur.com/DaUhVlP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Run command to list rules associated with the NSG.
<img src="https://i.imgur.com/2Gyb8j2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
<br />

<h4>Step 5: Create the network Security rule.</h4>
Run the command to create a rules that allows inbound access on port 80.
<img src="https://i.imgur.com/8i5S9sc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Verify the updated list of rules.
<img src="https://i.imgur.com/JaXnc5x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
<br />

<h4>Step 5: Access your web server again</h4>
Run the curl command to download the homepage
<img src="https://i.imgur.com/FC53XU1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
Download your IP Address, and access it via a web browser. The connection will suceed.
<img src="https://i.imgur.com/EUjUUpj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
<br />

