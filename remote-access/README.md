## What is Remote Access?  
A resource for employees to connect remotely using Azure Virtual Desktop (AVD), **Cisco AnyConnect VPN (also referred to as RESCUE)** or the Citrix Access Gateway (CAG).  

## What is Cisco AnyConnect VPN?  
Cisco AnyConnect is **a VPN that allows users to securely access company resources from their personal devices or company laptops, no matter where they are**. It's part of Cisco's SecureRemote Worker Solution and is designed to provide comprehensive protection and a consistent user experience across devices.  

The Cisco AnyConnect VPN client is for **government-issued laptops, desktops, and mobile devices only**. It is not a virtual desktop, but rather a direct VPN connection to the VA network and the primary method of connectivity for government-issued devices.  

## What is VPN?  
VPN is **a virtual private network (VPN) that creates a secure connection between a device and a remote server to protect a user's privacy and anonymity**. VPNs work by encrypting a user's internet connection and masking their IP address, which hides their identity, location, and browsing activity. This allows users to access web-based services and sites more securely, and can also help them bypass website blocks and firewalls, avoid being tracked online, and use public Wi-Fi more safely.   

## Request Remote Access (RESCUE)
Go to the RAP (Remote Access Portal)  
1.	Go to https://vaww.ramp.vansoc.va.gov/SelfService/Pages/RAUserDetails.aspx?val=n0rXTkvQi50dJEg08RXKKA==  

2.	Add New User  
a.	Enter any missing information and click Next  
b.	Enter a Justification (i.e. Need to work off-site) and click Next  
c.	Select your facility from a dropdown menu and click next  
d.	Select account type (i.e. Contractor or VA Employee) and click next  
e.	Select Company, search for your approving official and click next  
f.	Read the summary carefully and click next  

3.	Select type of Remote Access to Request  
a.	Under device type Select a VA-issued Laptop / Desktop  
b.	Under remote access methods select RESCUE Access  
c.	Click Submit  

## How to Test VPN Access  
If you need to log into Cisco AnyConnect Secure Mobility Client to connect to the VA network using RESCUE VPN, complete the following steps:   
1.	Insert the PIV into the card reader.  

2.	Click Cisco AnyConnect Secure Mobility Client, either using the Desktop icon or the bottom, right taskbar.  

3.	On the Cisco AnyConnect Secure Mobility Client window, click Connect.  

4.	When the Cisco AnyConnect – Certificate Selection window displays, select More choices to view certificates.  

5.	Under More choices, select the certificate as follows:  
a.	Choose the certificate with the farthest end date  
b.	Choose the certificate where the “Issuer” is “Department of Veterans Affairs CA”.  

6.	Click OK.  

7.	At the ActivClientLogon window, enter your Smartcard PIN and click OK. 

8.	Wait for Cisco AnyConnect to perform the security assessment.   
a.	When past the security assessment is complete. the system will log you into the VA network.    
b.	Keep your PIV in the reader to maintain the VPN connection. If your PIV card is removed, the connection will be lost.  

## Test VPN Access with PIV Exemption  
1. Open Cisco AnyConnect  

2. Go to settings (cog wheel)  

3. Click on the VPN tab  

4. Go to the Preference tab  
a. Uncheck Enable automatic VPN server selection
b. Close settings window  

5. Select a RESCUE NO_PIV sever  

6. Click on connect enter your user name and password  

7. Make sure your connection is successful

## Reinstall RESCUE VPN Software to Resolve Issues
1. Launch dBAT.exe.
   
2. Type the user's computer name in the Quick Search field and click on the Magnifying Glass icon.
   
3. Click the check box next to the computer name, and select Add To List.
   
4. Click the computer that has been added to the list, then click Scan Computer.
   
5. After the computer has been successfully scanned, click on the Tier 3/4 tab.
    
6. Select Cisco AnyConnect Secure Mobility Client and click Install/Uninstall.
    
7. When the install completes, the following Cisco AnyConnect applications will display in green text.
    
8. Reboot the computer to complete the installation.

## Request Citrix Access Gateway (CAG)
Go to the RAP (Remote Access Portal)  
1.	Go to https://vaww.ramp.vansoc.va.gov/SelfService/Pages/RAUserDetails.aspx?val=n0rXTkvQi50dJEg08RXKKA==
   
2.	Add New User.  
   a.	Enter any missing information and click Next  
   b.	Enter a Justification (i.e. Need to work off-site) and click Next  
   c.	Select your facility from a dropdown menu and click next  
   d.	Select account type (i.e. Contractor or VA Employee) and click next  
   e.	Select Company, search for your approving official and click next  
   f.	Read the summary carefully and click next  

3.	Select type of Remote Access to Request.  
   a.	Under device type Select Non-VA Device  
   b.	Under remote access methods select CAG Access  
   c.	Click Submit
  	
`Note:` CAG Access is normally use with Non-VA devices.  	

## Use your CAG Access
1. Go to https://citrixaccess.va.gov
   
2. Ensure you have a PIV card reader connected and your PIV card inserted (if you don’t have a badge, you must 
have an approved PIV exemption).

3. Select “Click here to use Smartcard” or “Domain Username/Password” option, a separate window will open.
   
4.  Enter your information. 
   a.Once your information is accepted, the window below will open  
   b. Click on “Accept” and access will be granted  
   c. Select 1VA-Clinical South or Southwest tab towards the bottom  
   d. A download tab will pop out (see below); ensure to select the most recent download request at the top of the list  
   e. If the above method doesn’t work, click on the 1VA-Clinical South icon to expand drop down option and click open 
   f. After clicking the download file, you will be taken to the VA network and desktop as if you were at the VA
   g. Click on V12 folder, then the STX programs folder, and finally the STX – GUI Executable to access Vista - R2, CPRSChart STX, 
and other needed programs  
 
5. To disconnect from the network click the down arrow (top middle of the page) and click on the disconnect option 
You will be taken to the window to log out, go to the settings icon to the top right corner and select Log off   
