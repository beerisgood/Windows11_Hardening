![GitHub last commit](https://img.shields.io/github/last-commit/beerisgood/Windows10_Hardening?label=last%20update%3A) ![enter image description here](https://img.shields.io/badge/for%20Windows:-20H2-blue)

This [*awesome tool*](https://github.com/AndyFul/Hard_Configurator) is highly recommend


# Requirements
- [x] [Standards](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure) for a highly secure Windows 10 device
- [x] System [up2date](https://support.microsoft.com/en-gb/help/4027667/windows-10-update) with latest [Windows 10 stable version](https://www.microsoft.com/en-us/software-download/windows10)
- [x] (default activated) and [Up2date](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus#monthly-platform-and-engine-versions) internal Microsoft Defender protection instead of external "Security" solutions
- [x] Latest Driver and Program updates
- [x] No "Tuning" tools (not even stuff like Ccleaner!)
- [x] Only necessary programs / apps / games which you realy need
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#requirements-met-by-system-guard-enabled-machines) for [System Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows) / [Hardware-based Isolation](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/overview-hardware-based-isolation)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/requirements-and-deployment-planning-guidelines-for-virtualization-based-protection-of-code-integrity#baseline-protections) for [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/memory-integrity)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard) for Microsoft [Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/wd-app-guard-overview) (WDAG)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-requirements) for Microsoft [Defender Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-how-it-works)


## Hardening
- [x] set User Account Control ([UAC](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-overview)) to [maximum](https://github.com/beerisgood/Windows10_Hardening/blob/master/maximum%20UAC%20level)
- [x] use Software Restriction Policies ([SRP](https://github.com/beerisgood/Windows10_Hardening/blob/master/Software%20Restriction%20Policies)) with a default-deny mode
- [x] use Defender [Firewall with Advanced Security](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)
- [x] Always [display](https://github.com/beerisgood/Windows10_Hardening/blob/master/always%20display%20file%20typ%20extension) file type extension
- [x] [Manage](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage) Microsoft Defender [Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard)
- [x] Install [Microsoft Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/install-wd-app-guard#install-application-guard) (WDAG)
- [x] Enable [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity#how-to-turn-on-hvci-in-windows-10) (HVCI)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection#powershell) Network Protection ([NP](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/network-protection))
- [x] Enable [SmartScreen](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device) and enable SmartScreen [Log](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#viewing-windows-event-logs-for-windows-defender-smartscreen)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-controlled-folders#powershell) Controlled Folder Access ([CFA](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/controlled-folders))
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#powershell) Attack Surface Reduction rules ([ASR](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction#attack-surface-reduction-rules))
- [x] [Harden](https://github.com/beerisgood/Windows10_Hardening/blob/master/harden%20ASLR) Address Space Layout Randomization ([ASLR](https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10#address-space-layout-randomization))
- [x] Enable [System Guard Secure Launch](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/enable-cloud-protection-windows-defender-antivirus)
- [x] [Activate](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus?ocid=wd-av-demo-pua-bottom#use-powershell-cmdlets-to-configure-pua-protection) Potentially unwanted applications ([PUA](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)) protection
- [x] Enable [Bitlocker Encryption](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10) with [Startup PIN](https://techcommunity.microsoft.com/t5/windows-10-security/hardening-windows-10-on-an-it-pro-s-laptop/m-p/183213/highlight/true#M232) & read about [Countermeasures](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-countermeasures) and reduce [DMA threats](https://support.microsoft.com/en-us/help/2516445/blocking-the-sbp-2-driver-and-thunderbolt-controllers-to-reduce-1394-d)
- [x] Use [Windows Sandbox](https://techcommunity.microsoft.com/t5/Windows-Kernel-Internals/Windows-Sandbox/ba-p/301849) for unknown/ untrusted binarys - [you can use it with right click menu](https://github.com/damienvanrobaeys/Run-in-Sandbox)!
- [x] [Enable sandboxing](https://www.microsoft.com/security/blog/2018/10/26/windows-defender-antivirus-can-now-run-in-a-sandbox/) for Microsoft Defender Antivirus
- [x] [Only elevate](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings#user-account-control-only-elevate-executables-that-are-signed-and-validated) executables which are signed and validated

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/specify-cloud-protection-level-windows-defender-antivirus#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] [Configure](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-exploit-protection#windows-security-app) Exploit [Protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/exploit-protection), like Edge 90+ with [enforced CET](https://techcommunity.microsoft.com/t5/windows-kernel-internals/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340#toc-hId--1650725290)
- [ ] Microsoft [recommended block rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] UEFI Hardening (NSA Defensive Practices Guidance) [PDF](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf) & Hardware-and-Firmware-Security-[Guidance](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance)
- [ ] Hardware and Firmware Security Guidance for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) & [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) - you will find more in the [overview](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance)
- [ ] Deploy [Windows Security Baselines](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-security-baselines) and keep it [up2date](https://www.microsoft.com/en-us/download/details.aspx?id=55319)
- [ ] use [Mandatory Integrity Control](https://docs.microsoft.com/en-us/windows/win32/secauthz/mandatory-integrity-control)

### For Enterprise/ Company only
- [ ] [Application Control](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control) (WDAC)
- [ ] [Enterprise Certificate Pinning](https://docs.microsoft.com/en-us/windows/access-protection/enterprise-certificate-pinning)
- [ ] [Block untrusted fonts in an enterprise](https://docs.microsoft.com/en-us/windows/threat-protection/block-untrusted-fonts-in-enterprise)
- [ ] [Web protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/web-protection-overview)
- [ ] [Protect](https://docs.microsoft.com/en-us/windows/security/identity-protection/remote-credential-guard) Remote Desktop credentials with Windows Defender Remote Credential Guard
- [ ] [Manage](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-manage-in-organization) Windows [Hello for Business](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-identity-verification)
- [ ] [Protect](https://attack.mitre.org/techniques/T1574/001/) against [DLL Search Order Hijacking](https://en.wikipedia.org/wiki/Dynamic-link_library#DLL_hijacking)

<br />

###### Test Config
- [Validate connections](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-network-connections-windows-defender-antivirus#validate-connections-between-your-network-and-the-cloud) between your network and the Microsoft Defender Antivirus cloud service
- [Verify client connectivity](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/configure-proxy-internet#verify-client-connectivity-to-microsoft-defender-atp-service-urls) to Microsoft Defender ATP service URLs
- [Validate](https://techcommunity.microsoft.com/t5/Microsoft-Defender-ATP/Tamper-protection-now-generally-available-for-Microsoft-Defender/ba-p/911482) Microsoft Defender Tamper protection
- [Confirm and validate](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-block-at-first-sight-windows-defender-antivirus#confirm-block-at-first-sight-is-enabled-with-the-windows-security-app) that Defender "Block at First Sight" (BAFS) is enabled
- Microsoft Defender [Testground](https://demo.wd.microsoft.com/)
- Microsoft Defender SmartScreen [Demo Pages](https://demo.smartscreen.msft.net/)
- Validate your [Kernel DMA Protection](https://docs.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt#how-to-check-if-kernel-dma-protection-is-enabled)
- [Test](https://malwaretips.com/threads/configuredefender-utility-for-windows-10.79039/page-37#post-837024) your Antimalware Scan Interface ([AMSI](https://docs.microsoft.com/en-us/windows/win32/amsi/antimalware-scan-interface-portal))
- [Test](https://smartscreentestratings2.net/) your Network protection
- [Changelogs](https://www.microsoft.com/en-us/wdsi/definitions/antimalware-definition-release-notes) for Defender security intelligence updates

<br />

###### Reading Material:
* https://github.com/frizb/Windows-Privilege-Escalation
* https://github.com/LOLBAS-Project/LOLBAS
* https://github.com/api0cradle/UltimateAppLockerByPassList
* https://trustedwindows.wordpress.com/
* https://docs.microsoft.com/en-us/windows-hardware/drivers/install/early-launch-antimalware
* https://www.microsoft.com/en-us/msrc/windows-security-servicing-criteria
* https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10
* https://docs.microsoft.com/en-us/windows/security/
* a [picture](https://www.microsoft.com/security/blog/wp-content/uploads/2020/08/fig1-pair-of-AMSI-machine-learning-models.png) about Microsoft Defender local and cloud script [protection](https://www.microsoft.com/security/blog/2020/08/27/stopping-active-directory-attacks-and-other-post-exploitation-behavior-with-amsi-and-machine-learning/)
* a [picture](https://raw.githubusercontent.com/beerisgood/Windows10_Hardening/master/Attack%20Surface%20Reduction%20(ASR)%20Rules.png) about Attack Surface Reduction (ASR) Rules
* Security Unlocked - The Microsoft Security [Podcast](https://securityunlockedpodcast.com/)
* How the hell WD works on Windows Home & Pro [documentation](https://malwaretips.com/threads/how-the-hell-wd-works-on-windows-home-pro.95146/) from [AndyFul](https://github.com/AndyFul)
* [Windows AppContainer Isolation - what it does?](https://malwaretips.com/threads/windows-appcontainer-isolation-what-it-does.90395/#post-797216) from AndyFul
* [Get to know](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/) the advanced technologies at the core of Microsoft Defender ATP next generation protection
* Windows Defender Application Control (WDAC) [Resources](https://medium.com/@mattifestation/windows-defender-application-control-wdac-resources-9cad7026a943)
* Why UAC is important at maximum (not default) level: [1](https://www.bleepingcomputer.com/news/security/trickbot-now-uses-a-windows-10-uac-bypass-to-evade-detection/), [2](https://www.bleepingcomputer.com/news/security/trickbot-uses-a-new-windows-10-uac-bypass-to-launch-quietly/), [3](https://www.fortinet.com/blog/threat-research/offense-and-defense-a-tale-of-two-sides-bypass-uac), [4](https://www.bleepingcomputer.com/news/security/bypassing-windows-10-uac-with-mock-folders-and-dll-hijacking/), ..
* [Testing DLL Search Order Hijacking against security features](https://malwaretips.com/threads/testing-dll-search-order-hijacking-against-security-features.101171/) from AndyFul
* Some info about [training AMSI machine learning models](https://malwaretips.com/threads/how-the-hell-wd-works-on-windows-home-pro.95146/page-4#post-935244) from AndyFul
* Cheap sandboxing with AppContainers [Blog](https://blahcat.github.io/2020/12/30/cheap_sandboxing_with_appcontainers/)
* Meet the Microsoft Pluton processor – The security chip designed for the future of Windows PCs [Blog](https://www.microsoft.com/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs/)
* Complete W^X implementation in Windows with [ACG](https://blogs.windows.com/msedgedev/2017/02/23/mitigating-arbitrary-native-code-execution/)
* Understanding [Hardware-enforced Stack Protection](https://techcommunity.microsoft.com/t5/windows-kernel-internals/understanding-hardware-enforced-stack-protection/ba-p/1247815) (CET)
* [Analysis](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP2/SiSyPHuS_AP2_node.html) of Windows 10 - OS Architecture
* [Analysis](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP5/SiSyPHuS_AP5_node.html) of TPM Integration and UEFI "Secure Boot" in Windows 10
* [Analysis](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP6/SiSyPHuS_AP6_node.html) of Virtual Secure Mode
* [Analysis](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP7/SiSyPHuS_AP7_node.html) of Device Guard
* [Analysis](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP8/SiSyPHuS_AP8_node.html) of Powershell and Windows Script Host
