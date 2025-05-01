## Imaging HP EliteBook 845 G8  
1.	Verify LT has been removed from AD (if out of the box, not needed)  

2.	Plug laptop into docking station.  Verify network cable and PWR supply are connected to docking station.  

3.	Turn on and F10 to BIOS Settings.  

4.	Main Tab Update BIOS to latest BIOS.  If Diagnostics come up, Exit and you will see BIOS.  

5.	It will restart after BIOS update. Power off after restart.  

6.	Turn on and F10 to BIOS Settings.  

7.	Date and Time – Update to current date and time. 

8.	Security Tab.  
  a.	TPM Embedded Security  
  b.	Check box for TPM State  
  c.	Clear TPM Security select On Next Boot  
  d.	Activation Policy – No Prompts  

9.	Arrow over to Advanced Tab.  
  a.	Click Boot Options  
  b.	Uncheck the first 2 boxes  
  c.	Check NUMlock on at boot  
  d.	Verify M.2 SSD1 is listed first under boot order  
  e.	Move USB below USB Network Boot  
  f.	Press ESC  

10.	Port Options.  
  a.	Uncheck Smart Card Power Savings  
  b.	Press ESC  

11.	Power Management Options.  
  a.	Check Power Control  
  b.	Let HP manage my battery charging  
  c.	Enable PSPP  
  d.	Press ESC to exit, Yes to save changes. Device will restart  

12.	Immediately upon restart, press F12 to enter the PXE Boot screen.  

13.	Select IPV4 - Network.  

14.	Press enter to continue.  
  a.	It will start loading files  

15.	When you see the screen all white, press Fn + F8 to Clean Disk (Not needed for new devices)
  a.	Type diskpart  
  b.	Type Select disk 0  
  c.	Type Clean  
  d.	Type Exit  
  e.	Type Exit  

16.	Welcome Task Sequence Wizard.  
  a.	Click next  
  b.	Select Image click next  
    i.	Currently PRD-1VA-Win10 -FU1809-P0520…. Production build  
  c.	Edit Task Sequence Variables  
    i.	Baseline: WIN10  
    ii.	District: Midwest  
    iii.	Site: NCH  
  d.	Click next  

17.	LT naming Conventions NCH-LTXXXXX (X=EE#).  

18.	Click next.  

19.	Click finished (make sure it says Central Time).  

20.	LT will begin to image.  

21.	LT image complete.  Will take appx. 3 hours.  
22.	Move LT to correct OU in AD from Test Lab>OSD Staging OU.  
  a.	Right-click on device  
  b.	Click on Properties  
  c.	Enter the following information under Description: Bldg 133EF / Room 3E210 / WIN10 / HP 845 G8 / RSS  
  d.	Click Apply and OK  
  e.	Right-click on device  
  f.	Click on Move  
  g.	Choose the following path: VISN12>North Chicago (NCH)>Laptops  

23.	Restart LTs.  

24.	Check that Bitlocker is on.  
  a.	Open Bitlocker
  b.	Make sure is ON  

25.	Logon to LT with Admin ACCT.  

26.	Copy and Paste Desktop Shortcuts.  
  a.	Go to \\v12.med.va.gov\v12\NCH\TechDrive\InformationTechnology\APPS\Laptop Bios & Drivers\HP EliteBook 845 G8\Desktop Shortcuts and Select all (CTL A), Copy all (CTL C)  
  b.	Go to c:\users\public\public desktop  
  c.	To see public desktop go to View and check Hidden items  
  d.	Paste the files (CTR V)  

27.	Install Drivers.
  a.	Go to \\v12.med.va.gov\v12\NCH\TechDrive \InformationTechnology\APPS\Laptop Bios & Drivers  
  b.	Open the folder for the model you’re installing  
  c.	Start at bottom of list and run each file.  Do NOT run HP Bios file since it has already been updated  

28.	Right click on battery icon, go to Power Options.  
  a.	Choose what closing the lid does  
  b.	On Battery – Do Nothing  
  c.	Plugged in – Do Nothing  
  d.	Save changes  

29.	Test VPN using PIV card.  
  a.	Open CiscoAnyConnect  
  b.	Click  Connect  
  c.	At window security click ok when you see your information  
  d.	At confirmation hit Ok  
  e.	Wait for System Scan to be completed  
  f.	You should be Connected and Compliant under status window  

30.	Run gp update command to Update Group Policy settings.    
  a.	Open terminal  
  b.	Type “gpupdate /force” on the command line  

31.	Restart LT.  

32.	Optional Install DMLSS (Defense Medical Logistics Standard Support ).
  a.	Go to \\v12.med.va.gov\v12\NCH\TechDrive \InformationTechnology\APPS  
  b.	Open dBat.exe  
  c.	The local workstation will show up on the left pane by default  
  d.	Click one on the local workstation or do a quick search for a remote workstation  
  e.	Scan computer and wait until status is completed  
  f.	Click on Tier/34 tab on third pane  
  g.	Check MHS DMLSS  
  h.	Click Install/Uninstall  
  i.	Click on install version on Action type selection for MHS DMLSS window  
  j.	Click OK  
  k.	Click ok on confirmation window  
  l.	The status will be on “Running” until completed  
  m.	Open DMLSS for testing  

## Imaging Dell Latitude 5430
Verify LT has been removed from AD
1. Verify Network cable and PWR supply connected to LT.
   
2. F12 Select BIOS Setup.
   
3. Click on the BIOS Setup tile.
   
4. Select Boot Configuration.  
  a. Check Boot Sequence  
    i. Windows Boot Manager  
    ii. UEFI PC SN740 NVMe WD512 GB  
    iii. ONBOARD NIC (IPV4)  
    iv. ONBOARD NIC (IPV6)  
    v. Uncheck SD Card Boot
   
5. Select Integrated Devices.  
  a. Check current time and date  
  b. Under USB/Thunderbolt Configuration  
  i. Uncheck USB Boot Support

6. Select Storage.  
  a. Under Enable MediaCard  
    i. Uncheck Secure Digital (SD) Card
   
7. Select Connection.  
  a. Under Wireless Device Enable  
    i. Uncheck WWAN/GPS  
  b. Under Enable UEFI Network Stack  
    i. Select Enable  
  c. Under HTTPS(s) Boot Feature/HTTP(s) Boot  
    i. Turn OFF (This platform has HTTP(s) Boot capabilities)
   
8. Select Security.  
  a. Under Clear TPM owner information  
    i. Turn ON (TPM owner information)
   
9. Select Update,Recovery.  
  a. Under Bios Recovery from Hard Drive  
    i. Turn OFF (Bios Recovery Hard Drive)
  b. Under Bios Downgrade  
    i. TURN OFF (Allow Bios Downgrade)  
  c. Under SupportAssist OS recovery  
    i. Turn OFF (SupportAssist OS recovery)  
  d. Under BiosConnect  
    i. Turn OFF (BiosConnect)  
  e. Under Dell Auto OS Recovery Threshold  
    i. Select OFF (Dell Auto OS Recovery Threshold)
   
10. Select System Management.  
  a. Under Intel AMT Capability  
    i. Toggle Disable (Enable Intel AMT Capability)  
  b. Under Diagnostics  
    i. Turn OFF (OS Agent Requests)  
  c. Under Power-on-Self-Test Automatic Recovery  
  Turn OFF (Power-on-Self-Test Automatic Recovery)

11. Select Pre-boot Behavior.  
  a. Under FastBoot  
    i. Select Thorough FastBoot  
  b. Under MAC Address Pass-Through  
    i. Select Disable (MAC Address Pass-Through)  
    
12. Select Virtualization Support.  
  a. Under DMA Protection  
    i. Turn OFF (Enable Pro-Boot DMA Support)
    
13. Click Apply.  
    
14. Click exit.
    
15. F12 at start up to PIXIE Boot.
    
16. Select IPV4.

17. Press enter to continue.
    
18. F8 to Clean Disk.  
  a. Type diskpart  
  b. Type Select disk 0  
  c. Type Clean  
  d. Type Exit  
  e. Type Exit

19. Welcome Task Sequence Wizard.  
  a. Click next  
  b. Select Image click next  
    i. Currently PRD-1VA-Windows 10 - Build 1810 - MS1709 Production  
  c. Edit Task Sequence Variables  
    i. Baseline: WIN10  
    ii. District: Midwest  
    iii. Site: NCH  
    iv. LT naming Conventions NCH-LTXXXXX (X=EE#)
    
20. Click Set.  
    
21. Click Continue.  
    
22. LT will begin to image.  
    
23. After LT image complete.  

24. Move LT to correct OU in AD from Test Lab>OSD Staging OU.  
  a. Right-click on device  
  b. Click on Properties  
  c. Enter the following information under Description: Bldg 133EF / Room 3E210 / WIN10 / HP 845 G8  
  d. Click Apply and OK  
  e. Right-click on device  
  f. Click on Move  
  g. Choose the following path: VISN12>North Chicago (NCH)>Laptops

25. Restart LTs.  

26. Check that Bitlocker is on.  
  a. Open Bitlocker  
  b. Make sure is ON

27. Logon to LT with Admin ACCT.
    
28. Copy and Paste Desktop Shortcuts.  
  a. Go to \\v12.med.va.gov\v12\NCH\TechDrive\InformationTechnology\APPS\Laptop Bios & Drivers\Dell Latitude 5430\Desktop Shortcuts and Select all (CTL A), Copy all (CTL C)  
  b. Go to c:\users\public\public desktop  
  c. To see public desktop go to View and check Hidden items  
  d. Paste the files (CTL V)

29. Install Drivers.  
  a. Go to \\v12.med.va.gov\v12\NCH\TechDrive\InformationTechnology\APPS\Laptop Bios & Drivers\Dell Latitude 5430 
  b. Open the folder for the model you’re installing  
  c. Start at bottom of list and run each file. Do NOT run HP Bios file since it has already been updated

30. Right click on battery icon, go to Power Options.  
  a. Choose what closing the lid does  
  b. On Battery – Do Nothing  
  c. Plugged in – Do Nothing  
  d. Save changes

31. Test VPN using PIV card.  
  a. Open CiscoAnyConnect  
  b. Click Connect  
  c. At window security click ok when you see your information  
  d. At confirmation hit Ok  
  e. Wait for System Scan to be completed  
  f. You should be Connected and Compliant under status window  

32. Run gp update command to Update Group Policy settings.  
  a. Open terminal  
  b. Type “gpupdate /force” on the command line

31. Restart LT.  
