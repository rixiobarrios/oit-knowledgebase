## What is BitLocker?  
BitLocker is **a Windows encryption feature** that protects data from unauthorized access by encrypting a computer's hard drive, including system files. It requires one or more factors of authentication to unlock, such as a PIN or removable device. BitLocker is often used in business settings, but it can also be used to improve the security of personal computers.

## Unlock BitLocker  
1.	From your computer, using your 0 account,  go to https://vaww.vambam.va.gov/helpdesk/  

2.	Put token in and enter pin.  

3.	Enter Other for reason.  Leave Domain and User ID blank.  

4.	Enter first 8 characters of the recovery key from locked computer, then Submit.  

5.	It will show this screen.  Type the generated Drive Recovery Key in to the computer that is locked.  

##  BitLocker TPM Issues  
Issue:	BitLocker continually asks for Recovery Key after reboots.  
Resolution:	Most likely the TPM module on the Motherboard doesn’t have the correct key.  The following steps should help reset this.  
 
1. Verify this scenario is the issue.  
  a. From an admin PowerShell prompt, type "tpm.msc" to open the TPM console  
  b. The console should state the issue  
 
2. When the keys do not match, you must clear the TPM and reboot to actually clear it.
   
3. Suspend Bitlocker first.  
  a. In PowerShell Type "Suspend-Bitlocker c: -rebootcount 1"  
  b. This will temporarily pause Bitlocker and auto enable it after 1 reboot  
 
 4. From the TPM console, select "Clear TPM" on the right hand side.  
  a. This will prompt you to reboot and inform you that you must accept the change before it can be cleared
  b. After the Reboot, you should see the TPM as ready for use  
`Note:`This may already be done when Bitlocker resumes, but verify by running the command.

5. Now you will need to Add the correct BitLocker key back to the TPM Module.  
  a. From Admin PowerShell Type "Add-Bitlockerkeyprotector c: -tpmprotector"  
