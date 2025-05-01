## Add a Network Printer
1. From the Printers & scanners menu, click the Add a printer or scanner button.

2. Windows searches the network for connected printers and lists its findings. Simply click the printer you want to connect to, then click Add device.

3. After conducting a search for a printer, click the printer that I want isn't listed to open a dialog box that will allow you to locate a printer by other means.  

4. Select "Add a printer using a IP address or hostname".
   a. This option brings up a new dialog box, where you'll need to enter the printer's hostname or IP address  
  
5. Click Next to connect your PC to the printer.

6. Once the installation is done, print a test page.                                                                                               

## Adding a Cerner Print Queue to a Printer  
1. Open up YourIT and Report an Issue.  
   
2. Scroll down and click on Report a New Issue.
   
3. Click on EHRM for the type of issue.
   
4. Click "Yes: I need to  submit a request to add or modify….."
   
5. Fill out the form. Note: I have been no been submitting on behalf of somebody else. However you'll need IP, Local Printer Name, Make/Model, Building/Room information.
    
6. Click Order Now.  

## Fixing a Hung Job in Print Queue
1. When you open up the print server/printer and go to cancel jobs and notice that one is still sitting there stuck at "deleting" at that moment the print spooler will need to be restarted.  

2. This is done by logging into the server (see desktop lead for information as IP's will not be listed here) going to the search menu and typing "services" then clicking "Print Spooler" and shutting it off.  

3. Once you turn it back on, give it a minute to initialize and the print job will disappear from the queue.  

``Note:`` If after this, it still isn't working as in the next test job gets stuck as well, restart the printer itself.  

## How to Access Print Servers
1. In the search bar at the bottom of the screen type "print management" and the print management console will appear, open it.  

2. Once open, right click "print servers" and click "add/remove servers".  

3. Under "add servers" type the following: R02NCHPRT01.  

4. Add to list, then click inside add servers again and add the other: Vhanchprt03.  

5. Add to list, after this you will now see the servers and you can navigate through them to find the printer you're looking for.  

