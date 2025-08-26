# How to set up a VPN for working remotely and blocking attackers
<p align="center">
<img width="197" height="215" alt="image" src="https://github.com/user-attachments/assets/fedcc81f-936b-41b2-88c7-1ff32248084d" />
</p>

<h1>VPN installation and Windows Powershell verification</h1>
This tutorial helps you to set up and change your vpn to various locations around the world. Then we will verify through powershell that the VPN is functioning properly within a virtual machine.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows Powershell

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create and Connect to a Windows Virtual Machine with Remote Desktop
- Download and Install VPN
- Turn On and allow Virtual Machine to connect and use VPN
- Create a VPN account
- Turn on VPN to a differnt country of choice
- Access to Windows Powershell

<h2>Installation Steps</h2>
<p></p>  
First you need to start off by creating a resource group within Microsoft Azure. I named the resource group FinalVPN and put my region as East US.
<p></p>

<img width="384" height="699" alt="image" src="https://github.com/user-attachments/assets/3dc4a303-d103-4767-a695-c004c2d51b31" />

Next you will have to create a virtual machine within Microsoft Azure. Be sure to use the same resource group name and region that you just created within this virtual machine.

<p></p>
<p>


<img width="825" height="691" alt="image" src="https://github.com/user-attachments/assets/e7e8cde0-0bd4-4e19-85b5-560386742a2b" />
</p>
<p>
Read carefully and make sure evertyhing you selected is corresponding with each other and choose an operating system size that has at least 8GB of ram. I chose the Windows 10 operating system V22H2

</p>
<br />

<p>
<img width="587" height="745" alt="image" src="https://github.com/user-attachments/assets/5b56df5e-7048-492d-b10a-ea564e00d167" />

  After everything has been created you will now see within your virtual machine the corresponding operating system along with a public IP address. 

</p>
<p>
</p>
<br />

<p>

<p></p>
<p></p>

<img width="883" height="542" alt="image" src="https://github.com/user-attachments/assets/10422cf2-a649-45c2-af2f-249b6e1a025a" />
</p>
<p>
Before you go into your Virtual Machine it would be best to set your ipconfiguration to static. This will prevent the private and public IP Addresses from changing over time. 

  <p></p>
  <p></p>
  <img width="640" height="758" alt="image" src="https://github.com/user-attachments/assets/4bef9345-874c-436e-bfe8-e716136aa916" />

Now it's time to connect to your virtual machine in Remote Desktop Connection. Sign on with the same user name and password you created within the virtual machine creation proccess. 
</p>
<br />
<img width="475" height="507" alt="image" src="https://github.com/user-attachments/assets/857da420-0756-4ba8-9658-a1f385122237" />

<p></p>
<p></p>

For this session I decided to create a VPN by the company PIA VPN. Withing the login for PIA VPN you want to install the correct Windows Operating system version which is Windows 10 64bit.
<p></p>
<p></p>


<img width="586" height="545" alt="image" src="https://github.com/user-attachments/assets/297e509d-c6ae-48b3-a2eb-38dd4898b405" />


<img width="566" height="211" alt="image" src="https://github.com/user-attachments/assets/e6fe3643-0544-43ff-bfc5-f927d5bd3e9d" />
<p></p>
<p></p>
Install the VPN on your computer. Next you want to go into your windows setting under VPN and allow your computer to be able to connect to the VPN. 

<p></p>
<p></p>
<img width="696" height="412" alt="image" src="https://github.com/user-attachments/assets/dea8f669-bb6c-404e-a4b8-b9c4e5c87cb8" />

<p></p>
<p></p>
As we can see our current IP address is now listed on the VPN server. We can also look up and double check our IP address on the web page whats my IP address. It will display the location of the IP address also.

<p></p>
<p></p>

<img width="302" height="441" alt="image" src="https://github.com/user-attachments/assets/cb49232f-3a37-441f-8e7b-e83c2823920b" />


<img width="776" height="581" alt="image" src="https://github.com/user-attachments/assets/6dcc1470-8086-4d3b-8019-65307a8cbb68" />
<p></p>
<p></p>
For my VPN I decided to choose Canada, Ontario. You can choose VPNs around the world but it's best to choose a vpn that has a fast speed if possible. After I selected and turned on the VPN I refreshed the page for what's my IP address and as you can see, it is now Canada.

<img width="398" height="518" alt="image" src="https://github.com/user-attachments/assets/85555b96-f420-4f48-b82f-68850a44bc28" />
<p></p>
<p></p>

To double check to make sure your VPN is securely active you can now access Windows Powershell. To make it simple I decided to use the command (Invoke-WebRequest -Uri "http://ifconfig.me/ip").Content. This will allow powershell to only display just the public IP address to get straight to the point. My first demonstration is with the VPN off.


<img width="557" height="43" alt="image" src="https://github.com/user-attachments/assets/8f7a28ab-a314-4895-a771-24f1e4f667fa" />
<p></p>
<p></p>

This is with the VPN on. I clicked around with my VPN just to have fun with changes so it is different from what is listed above. Now that we know that the VPN works properly we are sure that our true location is hidden and the computer cannot be hacked. I am now also able to work remotely from anywhere too now. 

<img width="621" height="36" alt="image" src="https://github.com/user-attachments/assets/80a29030-ec94-4e8f-b47c-14b1186b6eac" />

