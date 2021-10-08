![GitHub last commit](https://img.shields.io/github/last-commit/beerisgood/Windows11_Hardening?label=last%20update%3A) ![enter image description here](https://img.shields.io/badge/for%20Windows:-21H1-blue)

[*Hard_Configurator*](https://github.com/AndyFul/Hard_Configurator) is highly recommend and will save a lot of your time.


# Requirements
- [x] [Standards](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure) for a highly secure Windows device
- [x] System [up2date](https://support.microsoft.com/en-gb/help/4027667/windows-10-update) with latest [Windows stable version](https://www.microsoft.com/en-us/software-download/windows11)
- [x] (default activated) and [Up2date](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus#monthly-platform-and-engine-versions) internal Microsoft Defender protection instead of external "Security" solutions
- [x] Latest Driver and Program updates
- [x] No "Tuning" tools (not even stuff like Ccleaner!)
- [x] Only necessary programs / apps / games which you realy need
- [x] avoid insecure software like 7-Zip (which e.g. lacks [Anti-Exploit](https://malwaretips.com/threads/winrar-or-7zip-whats-your-favourite.89053/page-6#post-861699) and [MOTW](https://malwaretips.com/threads/winrar-or-7zip-whats-your-favourite.89053/page-3#post-800003) support), Open/ LibreOffice, [Firefox](https://madaidans-insecurities.github.io/firefox-chromium.html), [True/Veracrypt](https://github.com/beerisgood/Windows11_Hardening/blob/master/Why%20not%20use%20TrueCrypt-Veracrypt), ...
- [x] stay away from "Anti-Spying"/ "Anti-Telemetry"/.. tools and use [official documentation](https://github.com/beerisgood/Windows11_Privacy)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#requirements-met-by-system-guard-enabled-machines) for [System Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows) / [Hardware-based Isolation](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/overview-hardware-based-isolation)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/requirements-and-deployment-planning-guidelines-for-virtualization-based-protection-of-code-integrity#baseline-protections) for [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/memory-integrity)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard) for Microsoft [Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/wd-app-guard-overview) (WDAG)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-requirements) for Microsoft [Defender Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-how-it-works)


## Hardening
- [x] set User Account Control ([UAC](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-overview)) to [maximum](https://github.com/beerisgood/Windows11_Hardening/blob/master/maximum%20UAC%20level)
- [x] [create](https://support.microsoft.com/en-us/windows/create-a-local-user-or-administrator-account-in-windows-10-20de74e0-ac7f-3502-a866-32915af2a34d) another Admin account and [transform](https://www.windowscentral.com/how-change-user-account-type-windows-10#change-account-types-with-netplwiz) your current one to limited/ restricted/ standard user account to reduce the attack surface enormously. Don't use Admin account for your tasks!
- [x] use Software Restriction Policies ([SRP](https://github.com/beerisgood/Windows11_Hardening/blob/master/Software%20Restriction%20Policies)) with a default-deny mode
- [x] execute/ open new files with one-day-delay because after one day, the malware is not 0-day [anymore](https://malwaretips.com/threads/windows-defender-delay-protection.101566/#post-887769)
- [x] [block all incoming connections](https://malwaretips.com/threads/what-would-happen-if-a-legimate-program-os-or-game-somehow-had-a-virus-or-malware-installed-on-it-from-the-official-source.108861/page-2#post-949038) with Microsoft Defender Firewall
- [x] Always [display](https://github.com/beerisgood/Windows11_Hardening/blob/master/always%20display%20file%20typ%20extension) file type extension
- [x] [Manage](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage) Microsoft Defender [Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard)
- [x] Install [Microsoft Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/install-wd-app-guard#install-application-guard) (WDAG)
- [x] Enable [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity#how-to-turn-on-hvci-in-windows-10) (HVCI)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection#powershell) Network Protection ([NP](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/network-protection))
- [x] Enable [SmartScreen](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device) and enable SmartScreen [Log](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#viewing-windows-event-logs-for-windows-defender-smartscreen)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-controlled-folders#powershell) Controlled Folder Access ([CFA](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/controlled-folders))
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#powershell) Attack Surface Reduction rules ([ASR](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction#attack-surface-reduction-rules))
- [x] [Harden](https://github.com/beerisgood/Windows11_Hardening/blob/master/harden%20ASLR) Address Space Layout Randomization ([ASLR](https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10#address-space-layout-randomization))
- [x] Enable [System Guard Secure Launch](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/enable-cloud-protection-windows-defender-antivirus)
- [x] [Activate](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus?ocid=wd-av-demo-pua-bottom#use-powershell-cmdlets-to-configure-pua-protection) Potentially unwanted applications ([PUA](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)) protection
- [x] Enable [Bitlocker Encryption with TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10), optionally with [Startup PIN](https://techcommunity.microsoft.com/t5/windows-10-security/hardening-windows-10-on-an-it-pro-s-laptop/m-p/183213/highlight/true#M232) & read about [Countermeasures](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-countermeasures) and reduce [DMA threats](https://support.microsoft.com/en-us/help/2516445/blocking-the-sbp-2-driver-and-thunderbolt-controllers-to-reduce-1394-d)
- [x] Use [Windows Sandbox](https://techcommunity.microsoft.com/t5/Windows-Kernel-Internals/Windows-Sandbox/ba-p/301849) for unknown/ untrusted binarys - [you can use it with right click menu](https://github.com/damienvanrobaeys/Run-in-Sandbox) - or use [Virtual Machine](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/quick-create-virtual-machine) with [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/)
- [x] [Enable sandboxing](https://www.microsoft.com/security/blog/2018/10/26/windows-defender-antivirus-can-now-run-in-a-sandbox/) for Microsoft Defender Antivirus
- [x] [Only elevate](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings#user-account-control-only-elevate-executables-that-are-signed-and-validated) executables which are signed and validated
- [x] use the only browser on Windows [that natively supports](https://docs.microsoft.com/en-us/deployedge/ms-edge-security-for-business) hardware isolation: [Edge](https://www.microsoft.com/en-us/edge)
- [x] use [EFS file encryption](https://community.windows.com/en-us/stories/file-encryption-windows-10) for very sensitive files - also compatible with Bitlocker
- [x] (if OneDrive is used), [harden](https://malwaretips.com/threads/hard_configurator-windows-hardening-configurator.66416/page-28#post-743486) it with Windows CFA (Control Folder Access aka Ransomware Protection)
- [x] avoid old file systems like FAT32 as such format [does not preserve](https://malwaretips.com/threads/how-to-harden-my-system-against-usb-spreading-malware.98442/page-2#post-859762) Alternative NTFS Streams (Mark Of The Web is skipped)

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/specify-cloud-protection-level-windows-defender-antivirus#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] [Configure](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-exploit-protection#windows-security-app) Exploit [Protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/exploit-protection), like Edge 90+ with [enforced CET](https://techcommunity.microsoft.com/t5/windows-kernel-internals/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340#toc-hId--1650725290)
- [ ] Microsoft [recommended block rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] UEFI Hardening (NSA Defensive Practices Guidance) [PDF](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf) & Hardware-and-Firmware-Security-[Guidance](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance)
- [ ] Hardware and Firmware Security Guidance for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) & [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) - you will find more in the [overview](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance)
- [ ] Deploy [Windows Security Baselines](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-security-baselines) and keep it [up2date](https://www.microsoft.com/en-us/download/details.aspx?id=55319)
- [ ] use [Mandatory Integrity Control](https://docs.microsoft.com/en-us/windows/win32/secauthz/mandatory-integrity-control)
- [ ] [Custom ADMX template](https://github.com/Harvester57/Security-ADMX) focused on hardening Windows 10 systems

### Enterprise level
- [ ] [Application Control](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control) (WDAC) - Microsoft's [Policy Wizard](https://github.com/MicrosoftDocs/WDAC-Toolkit/blob/master/WDAC-Policy-Wizard/docs/getting-started/install-process.md) will help a lot
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
- check if your Bitlocker is safe against Bitleaker: [Blog](https://www.blackhat.com/asia-20/briefings/schedule/#bitleaker-subverting-bitlocker-with-one-vulnerability-19413)
- [Process Monitor](https://docs.microsoft.com/en-us/sysinternals/downloads/procmon) (tool from Microsoft) [filter](https://github.com/CERTCC/privesc) for finding privilege escalation vulnerabilities on Windows
- [winchecksec](https://github.com/trailofbits/winchecksec) performs static detection of common Windows security features
- Sysmon [configuration](https://github.com/SwiftOnSecurity/sysmon-config) file template with default high-quality event tracing

<br />

###### Reading Material:
* Defender [Firewall with Advanced Security](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)
* https://github.com/frizb/Windows-Privilege-Escalation
* https://github.com/LOLBAS-Project/LOLBAS
* https://github.com/api0cradle/UltimateAppLockerByPassList
* https://trustedwindows.wordpress.com/
* https://docs.microsoft.com/en-us/windows-hardware/drivers/install/early-launch-antimalware
* https://www.microsoft.com/en-us/msrc/windows-security-servicing-criteria
* https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10
* https://docs.microsoft.com/en-us/windows/security/
* a [picture](https://www.microsoft.com/security/blog/wp-content/uploads/2020/08/fig1-pair-of-AMSI-machine-learning-models.png) about Microsoft Defender local and cloud script [protection](https://www.microsoft.com/security/blog/2020/08/27/stopping-active-directory-attacks-and-other-post-exploitation-behavior-with-amsi-and-machine-learning/)
* a [picture](https://raw.githubusercontent.com/beerisgood/Windows11_Hardening/master/Attack%20Surface%20Reduction%20(ASR)%20Rules.png) about Attack Surface Reduction (ASR) Rules
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
* Threat Detection using Windows Defender Application Control (Device Guard) in Audit Mode [Blog](https://posts.specterops.io/threat-detection-using-windows-defender-application-control-device-guard-in-audit-mode-602b48cd1c11)
* [Security Unlocked](https://securityunlockedpodcast.com/) - The Microsoft Security Podcast about [Below the OS: UEFI Scanning in Defender](https://shows.acast.com/security-unlocked/episodes/below-the-os-uefi-scanning-in-defender)
* How the (Powershell) Constrained Language Mode is enforced [Blog](https://www.oreilly.com/library/view/learn-powershell-core/9781788838986/29834cd4-f9f3-4968-8493-ce4167214515.xhtml)
* Application Control denies execution of randomly generated PowerShell PS1 files [Blog](https://kc.mcafee.com/corporate/index?page=content&id=KB91608&locale=en_US)
* Applocker and PowerShell: how do they tightly work together? [Blog](https://p0w3rsh3ll.wordpress.com/2019/03/07/applocker-and-powershell-how-do-they-tightly-work-together/)
* PowerShell 5.0 and Applocker. When security doesn’t mean security [Blog](https://www.sysadmins.lv/blog-en/powershell-50-and-applocker-when-security-doesnt-mean-security.aspx)
* German BSI - [SiSyPHuS Win10](https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/SiSyPHuS_node.html): Study on System Integrity, Logging, Hardening and Security relevant Functionality in Windows 10
* rc3 event - [Breaking Thunderbolt 3 Security](https://media.ccc.de/v/rc3-534188-when_lightning_strikes_thrice)
* CIS [Security Benchmark](https://www.cisecurity.org/benchmark/microsoft_windows_desktop/)
* NIST Security Technical Implementation [Guide](https://ncp.nist.gov/checklist/629)
* AppLocker and WDAC help [Blog](https://improsec.com/tech-blog/one-thousand-and-one-application-blocks)
* Microsoft Defender Attack Surface Reduction (ASR) [recommendations](https://blog.palantir.com/microsoft-defender-attack-surface-reduction-recommendations-a5c7d41c3cf8)
* Adventures in Extremely Strict Device Guard (WDAC) Policy Configuration [Blog](https://posts.specterops.io/adventures-in-extremely-strict-device-guard-policy-configuration-part-1-device-drivers-fd1a281b35a8)
* Building a Simple, Secure Windows-only WDAC Policy [Blog](https://mattifestation.medium.com/windows-defender-application-control-wdac-updates-in-20h2-and-building-a-simple-secure-4fd4ee86de4)
* Application Control [on](https://malwaretips.com/threads/application-control-on-windows-10-home.89753/) Windows 10 Home
* Windows Hello - [Why a PIN is better than a password](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-why-pin-is-better-than-password)
* Battle of the SKM and IUM: How Windows 10 Rewrites OS Architecture ([blackhat USA 2015 talk](https://www.youtube.com/watch?v=LqaWIn4y26E))
* Defender (with [ConfigureDefender](https://github.com/AndyFul/ConfigureDefender/) tool) [vs](https://malwaretips.com/threads/configuredefender-utility-for-windows-10.79039/page-32#post-834160) fileless malware
* Offense and Defense – A Tale of Two Sides: [Bypass UAC](https://www.fortinet.com/blog/threat-research/offense-and-defense-a-tale-of-two-sides-bypass-uac)
