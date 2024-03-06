# queries

###CS advance search

The instance of AdobeARM.exe detected on the user's device is considered benign and is a part of normal operation, as it is associated with the Adobe Acrobat Update Service (Adobe Reader and Acrobat Manager, or ARM). The executable is confirmed to be legitimately signed by Adobe Systems Incorporated. Both AcroServicesUpdater2_x86.exe and RdrServicesUpdater2_x86.exe are executed by AdobeARM.exe. As of 06/03/2024, there is no evidence of malicious activity linked to this file on the user's device. However, it is worth noting that 8 vendors on VirusTotal have flagged RdrServicesUpdater2_x86.exe as suspicious. No immediate action is required, but continued monitoring for any unusual activities is recommended.



#$userlist = import-file -path c:\temp\userlist.txt
$userlist="VP33428", "V290694", "VP32928", "V291895", "V278383", "V175080", "V303467", "VP41675"
$results = foreach ($user in $userlist) { get-aduser -Identity $user -Properties SamAccountName, Enabled, LastLogonDate, PasswordLastSet }
$results | Export-CSV -LiteralPath C:\TEMP\User-Password-LastSet.csv -NoClobber -NoTypeInformation
