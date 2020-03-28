!**Work in progress / rebuild<br />
Any help is welcome**!
<br />

TL;DR: This [*awesome tool*](https://github.com/AndyFul/Hard_Configurator) do a lot stuff listed here

The Windows 10 [Secured-core PCs](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure) are also best start

# Requirements
- [x] [Standards](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure) for a highly secure Windows 10 device
- [x] Latest [Windows 10 stable version](https://www.microsoft.com/en-us/software-download/windows10)
- [x] System [up2date](https://support.microsoft.com/en-gb/help/4027667/windows-10-update)
- [x] (default activated) internal Windows Defender protection instead of external "Security" solutions
- [x] Latest Driver and Program updates
- [x] No "Tuning" tools
- [x] Only necessary tools which you realy need
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#requirements-met-by-system-guard-enabled-machines) for [System Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows) / [Hardware-based Isolation](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/overview-hardware-based-isolation)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/requirements-and-deployment-planning-guidelines-for-virtualization-based-protection-of-code-integrity#baseline-protections) for [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/memory-integrity)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard) for Windows [Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/wd-app-guard-overview) (WDAG)


## Hardening
- [x] Deploy latest [Microsoft Security Baseline](https://www.microsoft.com/en-us/download/details.aspx?id=55319) and keep it up2date
- [x] Install [Windows Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/install-wd-app-guard#install-application-guard) (WDAG)
- [x] Enable [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity#how-to-turn-on-hvci-in-windows-10) (HVCI)
- [x] Enable [network protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection#powershell)
- [x] Enable [SmartScreen](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device)
- [x] Enable [controlled folder access](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-controlled-folders#powershell)
- [x] Enable [attack surface reduction rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#powershell) (ASR)
- [x] Enable [System Guard Secure Launch](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/enable-cloud-protection-windows-defender-antivirus)
- [x] [Configure PUA protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection) in Windows Defender Antivirus
- [x] Enable [Bitlocker Encryption](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10)
- [x] Use [Windows Sandbox](https://techcommunity.microsoft.com/t5/Windows-Kernel-Internals/Windows-Sandbox/ba-p/301849) for test/ unknown/ untrusted binarys
- [x] [Enable sandboxing](https://www.microsoft.com/security/blog/2018/10/26/windows-defender-antivirus-can-now-run-in-a-sandbox/) for Windows Defender Antivirus
- [x] [Only elevate](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings#user-account-control-only-elevate-executables-that-are-signed-and-validated) executables that are signed and validated

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/specify-cloud-protection-level-windows-defender-antivirus#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] Configure [exploit protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-exploit-protection#windows-security-app)
- [ ] Microsoft [recommended block rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] UEFI Hardening (NSA Defensive Practices Guidance) [PDF](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf)
- [ ] Hardware and Firmware Security Guidance for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) & [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) - for other see the [overview](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance)

### For Enterprise/ Company only
- [ ] Configure [Application Control](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control)

<br />

###### Test Config
- [Validate connections](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-network-connections-windows-defender-antivirus#validate-connections-between-your-network-and-the-cloud) between your network and the Windows Defender Antivirus cloud service
- [Verify client connectivity](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/configure-proxy-internet#verify-client-connectivity-to-microsoft-defender-atp-service-urls) to Microsoft Defender ATP service URLs
- [Validate](https://techcommunity.microsoft.com/t5/Microsoft-Defender-ATP/Tamper-protection-now-generally-available-for-Microsoft-Defender/ba-p/911482) Windows Defender Tamper protection
- [Confirm and validate](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-block-at-first-sight-windows-defender-antivirus#confirm-block-at-first-sight-is-enabled-with-the-windows-security-app) that Defender "block at first sight" is enabled
- Windows Defender [Testground](https://demo.wd.microsoft.com/)
- Windows Defender SmartScreen [Demo Pages](https://demo.smartscreen.msft.net/)
- Validate your [Kernel DMA Protection](https://docs.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt#how-to-check-if-kernel-dma-protection-is-enabled)

<br />

###### Reading Material:
* https://github.com/frizb/Windows-Privilege-Escalation
* https://github.com/LOLBAS-Project/LOLBAS
* https://github.com/api0cradle/UltimateAppLockerByPassList
* https://trustedwindows.wordpress.com/
* https://docs.microsoft.com/en-us/windows-hardware/drivers/install/early-launch-antimalware
* https://www.microsoft.com/en-us/msrc/windows-security-servicing-criteria


<br />
All my commits are signed with my GPG Key:

ID 4AEE18F83AFDEB23 (0x620F071D)
<br />
Fingerprint: 3D3AA8EA763AA97DA252071497F9E213620F071D
