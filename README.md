

###CS advance search

The instance of AdobeARM.exe detected on the user's device is considered benign and is a part of normal operation, as it is associated with the Adobe Acrobat Update Service (Adobe Reader and Acrobat Manager, or ARM). The executable is confirmed to be legitimately signed by Adobe Systems Incorporated. Both AcroServicesUpdater2_x86.exe and RdrServicesUpdater2_x86.exe are executed by AdobeARM.exe. As of 06/03/2024, there is no evidence of malicious activity linked to this file on the user's device. However, it is worth noting that 8 vendors on VirusTotal have flagged RdrServicesUpdater2_x86.exe as suspicious. No immediate action is required, but continued monitoring for any unusual activities is recommended.


file://103.124.104.22/zjxb/bO.txt 
file://103.124.104.76/wsr6oh/Y.txt 
file://103.124.105.208/wha5uxh/D.txt 
file://103.124.105.233/yusx/dMA.txt 
file://103.124.106.224/uuny19/bb1nG.txt 
file://104.129.20.167/xhsmd/bOWEU.txt 
file://146.19.213.36/dbna/H.txt 
file://146.19.213.36/vei/yEZZ.txt 
file://155.94.208.137/tgnd/zH9.txt 
file://176.123.2.146/5aohv/9mn.txt 
file://176.123.2.146/vbcsn/UOx.txt 
file://66.63.188.19/bmkmsw/2.txt 
file://85.239.33.149/naams/p3aV.txt 
file://89.117.1.160/4bvt1yw/iC.txt 
file://89.117.1.160/zkf2r4j/VmD.txt 
file://89.117.1.161/epxq/A.txt 
file://89.117.1.161/mtdi/ZQCw.txt 
file://89.117.2.33/7ipw/7ohq.txt 
file://89.117.2.33/hvwsuw/udrh.txt 
file://89.117.2.34/3m3sxh6/IuM.txt 
file://89.117.2.34/4qp/8Y.txt 


(destination.ip: "103.124.104.22" OR destination.ip: "103.124.104.76" OR destination.ip: "103.124.105.208" OR destination.ip: "103.124.105.233" OR destination.ip: "103.124.106.224" OR destination.ip: "104.129.20.167" OR destination.ip: "146.19.213.36" OR destination.ip: "155.94.208.137" OR destination.ip: "176.123.2.146" OR destination.ip: "66.63.188.19" OR destination.ip: "85.239.33.149" OR destination.ip: "89.117.1.160" OR destination.ip: "89.117.1.161" OR destination.ip: "89.117.2.33" OR destination.ip: "89.117.2.34") 



---

C:\Windows\system32\wbem\wmiprvse.exe∅-Embedding

Based on our analysis, we consider the execution of wmiprvse.exe -Embedding to be benign. This command is a normal part of the Windows operating system's management infrastructure. There are no indications of suspicious behavior in this context, and we do not identify any immediate security threats from this activity. We will continue to monitor for any further unusual activities.


---

Here's a revised version of the note with a more cohesive and inclusive tone:

We have observed alerts in CrowdStrike related to the execution of VBCSCompiler.exe every time Visual Studio is opened. This executable is associated with the Roslyn Compiler used for compiling C# and Visual Basic projects. The user has noted that these alerts seem to be triggered by temporary libraries that are built during application execution. Although these files are expected to disappear once execution stops, Microsoft does not always clean up these files properly.

The user has been working on similar applications for years and mentioned that these alerts have only started appearing recently. The current project is expected to take at least 1 year to complete, if not more.

To address this issue, we will:

Verify that VBCSCompiler.exe is a legitimate part of the Visual Studio installation and not a malicious file.
Check if there have been any recent updates or changes to the CrowdStrike configuration that may have led to the increased sensitivity to VBCSCompiler.exe.
Consider adding an exception for VBCSCompiler.exe in the CrowdStrike policy if it is confirmed to be a false positive and necessary for the user's development workflow.
Monitor the situation and reassess if the alerts persist or if there are any changes to the user's development environment.
---
The file look like temp libraries that are being built when the app executes. They should disappear once execution stops. Microsoft doesn't always clean up after itself. I have been working on apps similar to the current one for years. It's just recently that these alerts are coming up. In anycase this project will likely take at least 1 year to complete if not more.

---

$userlist = Get-Content -Path "C:\Users\myname\OneDrive - COMPANY\Documents\userlist.txt"

$results = foreach ($user in $userlist) {
    Get-ADUser -Identity $user -Properties SamAccountName, Enabled, LastLogonDate, PasswordLastSet |
    Select-Object SamAccountName, Enabled, LastLogonDate, PasswordLastSet
}

$results | Export-Csv -LiteralPath "C:\Users\myname\OneDrive - COMPANY\Documents\User-Password-LastSet.csv" -NoTypeInformation

# How to Query Active Directory and Export User Information Using PowerShell

## Creating the User List File:

1. **Open Notepad or any text editor.**
2. **Enter the user IDs (SamAccountName), each on a new line.** For example:
3. **Save the file as `userlist.txt` in a directory of your choice.** For example, you can save it in any directory like `C:\TEMP` or your OneDrive folder.

## Running the PowerShell Script:

1. **Open PowerShell.**
2. **Copy and paste the following script into the PowerShell window:**
```powershell
$userlist = Get-Content -Path "\pathtoyourfile\userlist.txt"

$results = foreach ($user in $userlist) {
    Get-ADUser -Identity $user -Properties SamAccountName, Enabled, LastLogonDate, PasswordLastSet |
    Select-Object SamAccountName, Enabled, LastLogonDate, PasswordLastSet
}

$results | Export-Csv -LiteralPath "\pathtoyourfile\User-Password-LastSet.csv" -NoTypeInformation
```
Replace \pathtoyourfile\ with the actual path to your userlist.txt file.
3. Press Enter to run the script.

The results will be exported to a CSV file named User-Password-LastSet.csv in the same directory as your userlist.txt file.
Notes:
Make sure that the PowerShell execution policy allows you to run scripts. You can check the execution policy by running Get-ExecutionPolicy in PowerShell.
If you encounter any issues with the file path, ensure that the file is fully synced and available locally on your computer, especially when using cloud storage like OneDrive.
---

So the file MavInject32.exe is developed by Microsoft, native to the Windows operating system, and is used to inject DLLs into running processes. As MavInject32.exe can be used in a malicious manner (see: https://attack.mitre.org/techniques/T1218/) Falcon has logic to observe and alert upon its behavior.

The detections for MavInject32.exe you're referencing were triggered by a Microsoft update that leverages the file in a previously unseen way.

You may notice command line arguments in detections that look as follows:

"C:\Program Files\Common Files\Microsoft Shared\ClickToRun\mavinject32.exe" 10808 "C:\Program Files (x86)\Microsoft Office\root\Client\AppVIsvSubsystems32.dll" 1
The above argument injects AppVIsvSubsystems32.dll into the running process with PID 10808 and is part of some new Microsoft Office routine. We've updated the logic to account for this and sorry about the extra alerts this morning.

The impacting patch: Office 365 Client Update - Monthly Channel (Targeted) Version 1909 for x64 based Edition (Build 12026.20320)

"C:\WINDOWS\system32\SearchProtocolHost.exe" Global\UsGthrFltPipeMssGthrPipe4_ Global\UsGthrCtrlFltPipeMssGthrPipe4 1 -2147483646 "Software\Microsoft\Windows Search" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT; MS Search 4.0 Robot)" "C:\ProgramData\Microsoft\Search\Data\Temp\usgthrsvc" "DownLevelDaemon" 

Typically, you would only see MavInject32.exe loading DLLs from the system folder (oddly it's mostly audio drivers and similar) or trying to inject an attacker module into a running process as part of Defense Evasion/Execution.

Upon investigation, the alerts triggered by MavInject32.exe, clicktorun.exe, and SearchProtocolHost.exe are consistent with legitimate behavior associated with a Microsoft Office update and standard Windows Search operations. The observed command-line arguments and process activities align with known benign routines and do not exhibit malicious characteristics. Consequently, this incident alert in CrowdStrike can be confidently closed as a false positive, with no further action required.

---

winit.exe rclone
WizTree64.exe
svchost.exe rclone
AnyDesk.exe
DWAgent.exe
AcRes.exe

(ProcessName == 'winit.exe' and CommandLine contains 'rclone') or
ProcessName == 'WizTree64.exe' or
(ProcessName == 'svchost.exe' and CommandLine contains 'rclone') or
ProcessName == 'AnyDesk.exe' or
ProcessName == 'DWAgent.exe'


(cmdline:'winit.exe' AND cmdline:'rclone') OR proc_path:'WizTree64.exe' OR (cmdline:'svchost.exe' AND cmdline:'rclone') OR proc_path:'AnyDesk.exe' OR proc_path:'DWAgent.exe'
