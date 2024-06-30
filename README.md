![GitHub last commit](https://img.shields.io/github/last-commit/beerisgood/Windows11_Hardening?label=last%20update%3A&style=flat-square) ![recommend Windows version](https://img.shields.io/badge/for%20Windows:-23H2-blue)

[*Hard_Configurator*](https://github.com/AndyFul/Hard_Configurator) is a GUI application to configure various Windows security features and apply recommended defaults.

# Requirements
- [x] Minimum standards for a highly secure Windows device ([Secure-Core](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure))
- [x] Windows [up-to-date](https://www.microsoft.com/en-us/software-download/windows11)
- [x] Microsoft Defender [up-to-date](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/manage-updates-baselines-microsoft-defender-antivirus?view=o365-worldwide#monthly-platform-and-engine-versions)
- [x] Latest Driver and Program updates
- [x] Only necessary programs/apps/games which you need
- [x] avoid insecure software like 7-Zip (which lacks [Anti-Exploit](https://malwaretips.com/threads/winrar-or-7zip-whats-your-favourite.89053/page-6#post-861699) and [MOTW](https://malwaretips.com/threads/winrar-or-7zip-whats-your-favourite.89053/page-3#post-800003) support) and also [Forks](https://improsec.com/tech-blog/peazip-msi-installer-local-privilege-escalation-vulnerabilities), Open/ LibreOffice, [Firefox](https://madaidans-insecurities.github.io/firefox-chromium.html), [True/Veracrypt](https://github.com/beerisgood/Windows11_Hardening/blob/master/TrueCrypt-VeraCrypt), ...
- [x] stay away from "Anti-Spying"/"Anti-Telemetry"/.. tools and use [official documentation](https://github.com/beerisgood/Windows11_Privacy). Also instead of using insecure third-party "Windows tiny" tools, use Answer files ([unattend.xml](https://learn.microsoft.com/windows-hardware/manufacture/desktop/update-windows-settings-and-scripts-create-your-own-answer-file-sxs?view=windows-11)) from Microsoft.
- [x] No "Tuning" tools (not even stuff like Ccleaner!)
- [x] [Hardware Requirements](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#requirements-met-by-system-guard-enabled-machines) for [System Guard](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/how-hardware-based-root-of-trust-helps-protect-windows) / [Hardware-based Isolation](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/how-hardware-based-root-of-trust-helps-protect-windows?view=o365-worldwide)
- [x] [Hardware Requirements](https://learn.microsoft.com/en-us/windows/security/threat-protection/device-guard/requirements-and-deployment-planning-guidelines-for-virtualization-based-protection-of-code-integrity#baseline-protections) for [Memory integrity](https://support.microsoft.com/en-us/windows/core-isolation-e30ed737-17d8-42f3-a2a9-87521df09b78)
- [x] [Hardware Requirements](https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-requirements) for Microsoft [Defender Credential Guard](https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-how-it-works)


## Hardening
- [x] Set User Account Control ([UAC](https://learn.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-overview)) to [maximum](https://github.com/beerisgood/Windows11_Hardening/blob/master/maximum%20UAC%20level)
- [x] [Create](https://support.microsoft.com/en-us/windows/create-a-local-user-or-administrator-account-in-windows-20de74e0-ac7f-3502-a866-32915af2a34d) a different Admin account and [transform](https://www.windowscentral.com/how-change-user-account-type-windows-10/3) your current account to limited/restricted/standard user to reduce the attack surface enormously. Don't use administrator access for your tasks!
- [x] Use [Smart App Control](https://support.microsoft.com/en-us/topic/what-is-smart-app-control-285ea03d-fa88-4d56-882e-6698afdb7003)
- [x] [Block all incoming connections](https://web.archive.org/web/20210701053642/https://malwaretips.com/threads/what-would-happen-if-a-legimate-program-os-or-game-somehow-had-a-virus-or-malware-installed-on-it-from-the-official-source.108861/page-2#post-949038) with Microsoft Defender Firewall
- [x] Always [display file type extension](https://github.com/beerisgood/Windows11_Hardening/blob/master/always%20display%20file%20type%20extension)
- [x] [Manage](https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage) Microsoft Defender [Credential Guard](https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard)
- [x] Enable Memory Integrity ([HVCI](https://learn.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity#how-to-turn-on-hvci-in-windows-10))
- [x] Enable Network Protection ([NP](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/network-protection?view=o365-worldwide))
- [x] Enable [SmartScreen](https://learn.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-set-individual-device) and enable [SmartScreen Logs](https://learn.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview#viewing-windows-event-logs-for-windows-defender-smartscreen)
- [x] Enable Controlled Folder Access ([CFA](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/controlled-folders?view=o365-worldwide))
- [x] Enable Attack Surface Reduction rules ([ASR](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/attack-surface-reduction-rules-reference?view=o365-worldwide))
- [x] [Enable](https://github.com/beerisgood/Windows11_Hardening/blob/master/harden%20ASLR) Mandatory ALSR and Bottom-Up-ALSR ([Address Space Layout Randomization](https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10#address-space-layout-randomization))
- [x] Enable [System Guard Secure Launch](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/enable-cloud-protection-microsoft-defender-antivirus?view=o365-worldwide)
- [x] [Enable](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus?ocid=wd-av-demo-pua-bottom&view=o365-worldwide#use-powershell-cmdlets-to-configure-pua-protection) protection against Potentially Unwanted Apps ([PUA](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus?view=o365-worldwide#use-powershell-cmdlets-to-configure-pua-protection))
- [x] Enable [Bitlocker Encryption with TPM](https://learn.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10), optionally with [Startup PIN](https://techcommunity.microsoft.com/t5/windows-security/hardening-windows-10-on-an-it-pro-s-laptop/m-p/183213/highlight/true#M232) & read about [Countermeasures](https://learn.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-countermeasures) to reduce [DMA threats](https://support.microsoft.com/en-us/topic/blocking-the-sbp-2-driver-and-thunderbolt-controllers-to-reduce-1394-dma-and-thunderbolt-dma-threats-to-bitlocker-bf0ef10b-f563-5cfc-9740-8340b1d86a0c)
- [x] Use [Windows Sandbox](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/windows-sandbox/ba-p/301849) for new/unknown binaries ([you can use it with the right click menu](https://github.com/damienvanrobaeys/Run-in-Sandbox)) or enable [Hyper-V](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/) for use with Microsoft's [Virtual Machine Platform](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/quick-create-virtual-machine)
- [x] Enable [sandboxing](https://www.microsoft.com/en-us/security/blog/2018/10/26/windows-defender-antivirus-can-now-run-in-a-sandbox/) for Microsoft Defender Antivirus
- [x] [Only elevate executables which are signed and validated](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings#user-account-control-only-elevate-executables-that-are-signed-and-validated)
- [x] Use the only browser that [natively supports hardware isolation](https://docs.microsoft.com/en-us/deployedge/ms-edge-security-for-business): [Edge](https://www.microsoft.com/en-us/edge)
- [x] Use [EFS file encryption](https://community.windows.com/en-us/stories/file-encryption-windows-10) for very sensitive files - also compatible with Bitlocker
- [x] [Harden OneDrive](https://malwaretips.com/threads/hard_configurator-windows-hardening-configurator.66416/page-28#post-743486) with Windows Controlled Folder Access ([CFA](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/controlled-folders?view=o365-worldwide) aka Ransomware Protection)
- [x] Avoid old file systems like FAT32 that [do not preserve Alternative NTFS Streams](https://malwaretips.com/threads/how-to-harden-my-system-against-usb-spreading-malware.98442/page-2#post-859762) (where Mark Of The Web is skipped)
- [x] While DNS encryption [isn't perfect](https://madaidans-insecurities.github.io/encrypted-dns.html) both [Quad9](https://www.quad9.net) and [Cloudflare](https://developers.cloudflare.com/1.1.1.1/setup/) are recommend. [AdGuard](https://adguard-dns.io) and [NextDNS](https://nextdns.io/) are another, but some users report problems like false positive filtering, stability/performance issues.
- [x] instead of passwords, use [Passkeys](https://support.microsoft.com/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422)

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/specify-cloud-protection-level-microsoft-defender-antivirus?view=o365-worldwide#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] [Configure](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/enable-exploit-protection?view=o365-worldwide#windows-security-app) Microsoft's [Exploit Protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/exploit-protection) and [Enforced CET](https://techcommunity.microsoft.com/t5/windows-kernel-internals/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340#toc-hId--1650725290)
- [ ] Use [Microsoft's recommended block rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] See UEFI Hardening aka [NSA Defensive Practices Guidance](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf) and [Hardware-and-Firmware-Security-Guidance](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance)
- [ ] See [Hardware and Firmware Security Guidance](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance) for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) and [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) 
- [ ] Deploy [Windows Security Baselines](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-security-configuration-framework/windows-security-baselines) and keep it [up-to-date](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
- [ ] Use [Mandatory Integrity Control](https://learn.microsoft.com/en-us/windows/win32/secauthz/mandatory-integrity-control)
- [ ] Use [Security-ADMX custom template](https://github.com/Harvester57/Security-ADMX) focused on hardening Windows 10 systems

### Enterprises
- [ ] [Application Control](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control) (WDAC) - Microsoft's [Policy Wizard](https://github.com/MicrosoftDocs/WDAC-Toolkit/blob/master/WDAC-Policy-Wizard/docs/getting-started/install-process.md) will help a lot
- [ ] [Enterprise Certificate Pinning](https://learn.microsoft.com/en-us/windows/security/identity-protection/enterprise-certificate-pinning)
- [ ] [Block untrusted fonts in an enterprise](https://learn.microsoft.com/en-us/windows/security/threat-protection/block-untrusted-fonts-in-enterprise)
- [ ] [Web protection](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/web-protection-overview?view=o365-worldwide)
- [ ] [Protect](https://learn.microsoft.com/en-us/windows/security/identity-protection/remote-credential-guard) Remote Desktop credentials with Windows Defender Remote Credential Guard
- [ ] [Manage](https://learn.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-manage-in-organization) Windows [Hello for Business](https://learn.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-identity-verification)
- [ ] [Protect](https://attack.mitre.org/techniques/T1574/001/) against [DLL Search Order Hijacking](https://en.wikipedia.org/wiki/Dynamic-link_library#DLL_hijacking)
- [ ] [Report](https://www.microsoft.com/en-us/wdsi/driversubmission) vulnerable or malicious drivers to the Windows and Defender teams
- [ ] [Video](https://www.youtube.com/watch?v=SQwVSgdFBFs) from Matt Soseman: Investigating Backdoor Attacks w/ Microsoft Defender ATP
- [ ] [Video](https://www.youtube.com/watch?v=e3TGejjVyog) from Matt Soseman: Investigating a Fileless Attack w/ Microsoft Defender ATP & Exploit Protection
- [ ] [Video](https://www.youtube.com/watch?v=CcN7EEpOgNw) from Matt Soseman: What is the Microsoft Cybersecurity Reference Architectures (MCRA) and why should I care?
- [ ] Microsoft Defender ATP [secure score](https://malwaretips.com/threads/configuredefender-utility-for-windows-10.79039/page-20#post-809699)
- [ ] Microsoft Edge [for Business](https://www.microsoft.com/en-us/edge/business?form=MA13FJ)
<br />

###### Test Config
- [Validate connections](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/configure-network-connections-microsoft-defender-antivirus?view=o365-worldwide#validate-connections-between-your-network-and-the-cloud) between your network and the Microsoft Defender Antivirus cloud service
- [Verify client connectivity](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/configure-proxy-internet?view=o365-worldwide#verify-client-connectivity-to-microsoft-defender-atp-service-urls) to Microsoft Defender ATP service URLs
- [Validate](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/tamper-protection-now-generally-available-for-microsoft-defender/ba-p/911482) Microsoft Defender Tamper protection
- [Confirm and validate](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/configure-block-at-first-sight-microsoft-defender-antivirus?view=o365-worldwide#confirm-block-at-first-sight-is-enabled-with-the-windows-security-app) that Defender "Block at First Sight" (BAFS) is enabled
- Microsoft Defender [Testground](https://demo.wd.microsoft.com/)
- Microsoft Defender SmartScreen [Testground](https://demo.smartscreen.msft.net/)
- Validate your [Kernel DMA Protection for Thunderbolt](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt#how-to-check-if-kernel-dma-protection-is-enabled)
- [Test](https://malwaretips.com/threads/configuredefender-utility-for-windows-10.79039/page-37#post-837024) your Antimalware Scan Interface ([AMSI](https://learn.microsoft.com/en-us/windows/win32/amsi/antimalware-scan-interface-portal) your Network protection
- [Changelogs](https://www.microsoft.com/en-us/wdsi/definitions/antimalware-definition-release-notes) for Defender security intelligence updates
- Check if your Bitlocker is safe against Bitleaker: [Blog](https://www.blackhat.com/asia-20/briefings/schedule/#bitleaker-subverting-bitlocker-with-one-vulnerability-19413)
- Use [Process Monitor](https://learn.microsoft.com/en-us/sysinternals/downloads/procmon) (tool from Microsoft) with [this filter](https://github.com/CERTCC/privesc) for finding privilege escalation vulnerabilities in Windows
- Check out [winchecksec](https://github.com/trailofbits/winchecksec) to perform static detection of common Windows security features
- Sysmon [configuration](https://github.com/SwiftOnSecurity/sysmon-config) file template with default high-quality event tracing
- check your installation against [Deprecated features](https://learn.microsoft.com/en-us/windows/whats-new/deprecated-features#deprecated-features)

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
* [Get to know](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/) the advanced technologies at the core of Microsoft Defender ATP next-generation protection
* Windows Defender Application Control (WDAC) [Resources](https://medium.com/@mattifestation/windows-defender-application-control-wdac-resources-9cad7026a943) / [PowerShell script](https://github.com/mattifestation/WDACTools)
* Why UAC is important at maximum (not default) level: [1](https://www.bleepingcomputer.com/news/security/trickbot-now-uses-a-windows-10-uac-bypass-to-evade-detection/), [2](https://www.bleepingcomputer.com/news/security/trickbot-uses-a-new-windows-10-uac-bypass-to-launch-quietly/), [3](https://www.fortinet.com/blog/threat-research/offense-and-defense-a-tale-of-two-sides-bypass-uac), [4](https://www.bleepingcomputer.com/news/security/bypassing-windows-10-uac-with-mock-folders-and-dll-hijacking/)
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
* PowerShell 5.0 and Applocker. When security doesn't mean security [Blog](https://www.sysadmins.lv/blog-en/powershell-50-and-applocker-when-security-doesnt-mean-security.aspx)
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
* Microsoft Windows Antimalware Scan Interface (AMSI) [Bypasses](https://thalpius.com/2021/10/14/microsoft-windows-antimalware-scan-interface-bypasses/)
* Windows security book in [web doc form](https://docs.microsoft.com/en-us/windows/security/)
* [Video](https://www.youtube.com/watch?v=UW71JGE6Nsc) from Matt Soseman: Smartscreen in Edge (& Chrome) to block phishing & malicious websites
* [Video](https://www.youtube.com/watch?v=fkKKuzhe1fE) from Matt Soseman: Block at First Sight (BAFS): Windows Defender blocking malware in SECONDS!
* [Video](https://www.youtube.com/watch?v=qgaRGaLd7-o) from Matt Soseman: How Controlled Folder Access (CFA) works in Windows
* [Video](https://www.youtube.com/watch?v=QktCmzrqOp4) from Matt Soseman: Block Potentially Unwanted Applications (PUA) in Microsoft Defender Antivirus
* [Video1](https://www.youtube.com/watch?v=36OJHS-4VhE), [Video2](https://www.youtube.com/watch?v=j5MaWilThkY) from Matt Soseman: Attack Surface Reduction (ASR) in Windows
* [Video](https://www.youtube.com/watch?v=OFEdoCWZjaI) from Matt Soseman: Hardware Isolated Browsing w/ Microsoft Defender Application Guard
* what is meant by "[User Space](https://malwaretips.com/threads/run-by-smartscreen-utility.65145/#post-561364)"
* what the feature "Allow apps from the store only" [does](https://malwaretips.com/threads/use-windows-10-build-in-anti-execution-options.85477/#post-752441)
* [Breaking](https://www.youtube.com/watch?v=wTl4vEednkQ) Bitlocker - Bypassing the Windows Disk Encryption / [more](https://github.com/Wack0/bitlocker-attacks) BitLocker Attacks
* Zammis Clark: An Evil Maid's Dream - Windows Boot Security was Broken [Anyway](https://www.youtube.com/watch?v=U02ClZS8hqw)
* [Harden](https://github.com/HotCakeX/Harden-Windows-Security) Windows Safely
* inside the Copilot+ [Recall disaster](https://doublepulsar.com/recall-stealing-everything-youve-ever-typed-or-viewed-on-your-own-windows-pc-is-now-possible-da3e12e9465e)
* help and ideas [for](https://schneegans.de/windows/unattend-generator/) answer files (typically named unattend.xml or autounattend.xml)
