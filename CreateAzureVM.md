Required
========
*** Make a Resource Group of "DomEntChall" or change the variable on line 33 to a resource group that exists in your Azure account ***

Code
====
The code is located on GitHub at 
  https://github.com/LenChaney/Dominion-Enterprises-Scripting-Challenge
I'm not sure what your email system will strip out but at a minimum, script files would get it.

Powershell
==========
Version: 
  Microsoft Azure PowerShell 
  Version: 5.3.0 
  Date: 13 Feb 2018
installed through Web Platform Installer


Azure
=====
I used an interactive login.  You should be able to use your own Azure account although I can get you my developer credentials in needed

Coordinating instructions
=========================
Hardcoded Values
Resource Group DomEntChall
Location: East US
VM Size: A0 Standard - I allowed you to choose but to avoid mistakes and shorten testing, use smallest and least expensive option.
OS: 2016 Datacenter latest version  - ovviously it could be a lot more choices and those choices could be dynamic but in a corp enviroment, the choices would necessarily be restricted.
vNic, Security Resource Group, and PublicDNS will have a randomized postfix so there is no conflict. I could have done this better or more appropriately use a standard name.  There may be conflict with making a second VM without removing the first

Running the Script
==================
Note: Script take a while to run but that time appears to be Azure creating the VM

1. Make a Resource Group of DomEntChall or change the variable to a resource group that exists in your Azure account
2. Run CreateAzureVM.ps1
3. Logon with Azure credentials
4. Create credentials for the new server
5. Choose a size for the VM from this limited list of standard sizes
6. Choose a name or hit enter for the default
7. Review choices and hit enter to continue
8. Wait
Note the output because that will have the IP address of the new VM although you can get it in the Azure portal

Other
=====
Port 3389 is open for RDP
VM account user name should not indluce "Admin" or any standard name.
Password length in portal is 12 characters min although the script appears to work with less

RandomId will be 3 characters between 100 and 999
Servername is max of 15 characters
I included the function of Show-VMSizeManu to demonstrate that I know how to use Functions

