# IntuneDebugToolkit

Please go and visit MSEndpointMgr -> solutions -> Intune Debug Toolkit

***

Here is a demo of how I use the Win32 rerun tool. Pssssttt there are a description of all the other tools on the MSEndpointMgr Site!
VLOG on how to rerun win32 apps here and now:

[![Rerun win32 apps](https://github.com/mmelkersen/EndpointManager/blob/main/Intune%20Debug%20Tools/Content/hqdefault.jpg)](https://www.youtube.com/watch?v=gHG84MKE5O4 "Rerun Win32 apps")


# History

### Version 2.0
- updated SyncMLViewer from v1.0.7 to v1.0.8 (Read more about the changes here [Oliver's github](https://github.com/okieselbach/SyncMLViewer "Oliver Kieselbach"))
- added script to help transition to Windows Update for Business and to find troublemaking policies interfering with the best configuration. (Read more about the script here [Mattias's github](https://github.com/mmelkersen/EndpointManager/tree/main/Windows%20Update%20for%20Business "Mattias Melkersen"))
- added reference to error codes and solutions of Microsoft Intune ([Mattias's blog](https://blog.mindcore.dk/2022/09/intune-error-codes-and-solutions/ "Mattias Melkersen"))
- added Rudy Ooms AutopilotTestAttestation script to check if your device is ready for pre-provisioning. (Read more about the solution here [Rudy's blog](https://call4cloud.nl/2022/08/the-last-tpm-attestation-script-from-your-lover/ "Rudy Ooms"))
- added easy Intune diagnostic export [David Just](https://github.com/djust270/IntuneEndpointTools "David Just"))
- added autopilot precheck [Jannik Reinhard](https://jannikreinhard.com/2022/08/24/check-autopilot-enrollment-prerequisite/ "Jannik Reinhard"))
- added Proactive remediation reader, Win32AppRedeploy and Intune RSOP [Andrew](https://www.powershellgallery.com/packages/IntuneStuff/1.1.7 "Andrew"))
- rebranded and created as a solution on MSEndpointMgr site.

---

### Version 1.5
- Added new functionality to get and continue read the relevant eventlog messages you need in order to debug settings comming down to your client.

This tool will reveal any issues written to the eventlog. Events followed:
- Microsoft-Windows-DeviceManagement-Enterprise-Diagnostics-Provider/Admin
- Microsoft-Windows-DeviceManagement-Enterprise-Diagnostics-Provider/Operational
- Microsoft-Windows-ModernDeployment-Diagnostics-Provider/Autopilot
- Microsoft-Windows-ModernDeployment-Diagnostics-Provider/ManagementService
- Microsoft-Windows-Provisioning-Diagnostics-Provider/Admin
- Microsoft-Windows-Shell-Core/Operational
- Microsoft-Windows-Time-Service/Operational
- Microsoft-Windows-User Device Registration/Admin

A big thanks to [David Segura](https://twitter.com/SeguraOSD "David Segura") OSDCloud where this code is from.

---

### Version 1.4
- Added Petri Paavola's Intune Device Detail tool to the kit. Thanks for allowing me to add this tool, [Petri](https://twitter.com/petripaavola "Petri Paavola")

This tool visualizes Intune device and user details and Applications and Configurations Deployment
This tools offers Resultant Set Of Policy -type view for Intune

Get more information about the tool [Here](https://github.com/petripaavola/IntuneDeviceDetailsGUI "Petri Paavola")

---

### Version 1.3
- Added icons on all shortcuts
- Added Oliver Kieselbach's SyncMLViewer debug tool to the kit. Thanks for allowing me to add this tool, [Oliver](https://twitter.com/okieselb "Oliver Kieselbach")

This tool is able to present the SyncML protocol stream between the Windows 10 client and management system. In addition it does some extra parsing to extract details and make the analyzing a bit easier.
The tool uses ETW to trace the MDM Sync session. In general the tool can be very handy to troubleshoot policy issues. Tracing what the client actually sends and receives provides deep protocol insights.
It makes it easy to get confirmation about queried or applied settings. Happy tracing!

Get more information about the tool [Here](https://github.com/okieselbach/SyncMLViewer "Oliver Kieselbach Github")

---

### Version 1.2
- Added -executionpolicy bypass on all shortcuts

---

### Version 1.1
What is this addon going to help with?
- What if you added a policy from Intune and wanted to see where it added values on the device?
- What if you wanted to know if IME is actually is refreshing its registry and check for the installed apps are installed?
- Did anyone push new GPO's policies to your device? If you are transitioning to Intune with hybrid identity you like to know what goes on.

Added 5 shortcuts to view registry changes from the last 36 hours. (could be done via sysinternals tools. This is just so much easier.)
- Shortcut1: DEBUG - GPO changes last 36 hours (looking for changes in registry: HKLM:\Software\policies)
- Shortcut2: DEBUG - Enrollment changes last 36 hours (looking for changes in registry: HKLM:\Software\Microsoft\Enrollments)
- Shortcut3: DEBUG - IME changes last 36 hours (looking for changes in registry: HKLM:\Software\Microsoft\IntuneManagementExtension)
- Shortcut4: DEBUG - PolicyManager changes last 36 hours (looking for changes in registry: HKLM:\Software\Microsoft\PolicyManager)
- Shortcut5: DEBUG - ALL MS registry changes last 36 hours (OBS takes time to run - looking for changes in registry: HKLM:\Software\Microsoft)

> [!NOTE]
> Script reference: https://github.com/guyrleech/General-Scripts/blob/master/Regrecent.ps1

---

### Version 1.0
First release of the debug tool containting rerun win32 apps.

> [!NOTE]
> Script reference: https://github.com/ztrhgf/useful_powershell_functions/blob/master/INTUNE/Invoke-IntuneWin32AppRedeploy.ps1