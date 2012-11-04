About
=====

This Powershell module contains a collection of functions gathered from an assortment of scripts I use to automate SCCM 2007 management.  I realized that every time I needed to automate something I ended up digging through a pile of old scripts to cut and paste code into a new one, so eventually I decided I needed to aggregate all of the bits of code I had created into a single script.  This module does not encompass a large part of client management functions in SCCM, but it can perform a number of common operations such as creating new computer records, deleting them, and manipulating collection membership rules.

These are the functions currently present in the module:

* New-SCCMComputer
* Remove-SCCMComputer
* Get-SCCMComputer
* Add-SCCMComputerToCollection
* Remove-SCCMComputerFromCollection
* Get-SCCMCollection
* Get-SCCMCollectionsForComputer
* Get-SCCMAdvertisementsForCollection
* Get-SCCMAdvertisementsForComputer
* Get-SCCMAdvertisementStatusForComputer
* Set-SCCMComputerVariable
* Get-SCCMComputerVariables
* Remove-SCCMComputerVariable
* Invoke-SCCMClientAction
* Invoke-SCCMClientSchedule
* Get-SCCMClientAdvertisementHistoryForComputer
* Get-SCCMClientAdvertisementScheduleId
* Get-SCCMClientAssignedSite
* Set-SCCMClientAssignedSite
* Convert-SCCMDate
* Get-SCCMPackage
* Get-SCCMProgram

This code has only been tested with SCCM 2007.  Please conduct your own independent testing before trusting this code in a production environment.

Installation
============

Run the Install.ps1 script provided with the module.  Alternatively, create the directory:

    %userprofile%\Documents\WindowsPowershell\Modules\SCCM

After creating the directory, copy the SCCM.psm1 file into it.

Usage
=====

Use the following line at the top of your scripts:
    
    Import-Module SCCM

If the import is successful, you should be able to use all of the module's exported functions.  To see a list of available functions, use:

    Get-Help SCCM