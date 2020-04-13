This [*awesome tool*](https://github.com/AndyFul/Hard_Configurator) is highly recommend

Here now Windows internal Hardening features:


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
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-requirements) for Windows [Defender Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-how-it-works)


## Hardening
- [x] set User Account Control ([UAC](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-overview)) to [maximum](https://github.com/beerisgood/Windows10_Hardening/blob/master/maximum%20UAC%20level)
- [x] use Defender [Firewall with Advanced Security](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)
- [x] Always [display](https://github.com/beerisgood/Windows10_Hardening/blob/master/always%20display%20file%20typ%20extension) file type extension
- [x] [Manage](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage) Windows Defender [Credential Guard](https://docs.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard)
- [x] Install [Windows Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/install-wd-app-guard#install-application-guard) (WDAG)
- [x] Enable [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity#how-to-turn-on-hvci-in-windows-10) (HVCI)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection#powershell) Network Protection ([NP](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/network-protection))
- [x] Enable [SmartScreen](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device) and enable SmartScreen [Log](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#viewing-windows-event-logs-for-windows-defender-smartscreen)
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-controlled-folders#powershell) Controlled Folder Access ([CFA](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/controlled-folders))
- [x] [Enable](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#powershell) Attack Surface Reduction rules ([ASR](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction#attack-surface-reduction-rules))
- [x] [Harden](https://github.com/beerisgood/Windows10_Hardening/blob/master/harden%20ASLR) Address Space Layout Randomization ([ASLR](https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10#address-space-layout-randomization))
- [x] Enable [System Guard Secure Launch](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/enable-cloud-protection-windows-defender-antivirus)
- [x] [Activate](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus?ocid=wd-av-demo-pua-bottom#use-powershell-cmdlets-to-configure-pua-protection) Potentially unwanted applications ([PUA](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)) protection
- [x] Enable [Bitlocker Encryption](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10) with [Startup PIN + TPM](https://techcommunity.microsoft.com/t5/windows-10-security/hardening-windows-10-on-an-it-pro-s-laptop/m-p/183213/highlight/true#M232) instead of TPM only and read about other [Countermeasures](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-countermeasures)
- [x] Use [Windows Sandbox](https://techcommunity.microsoft.com/t5/Windows-Kernel-Internals/Windows-Sandbox/ba-p/301849) for unknown/ untrusted binarys - [you can use it with right click menu](https://github.com/damienvanrobaeys/Run-in-Sandbox)!
- [x] [Enable sandboxing](https://www.microsoft.com/security/blog/2018/10/26/windows-defender-antivirus-can-now-run-in-a-sandbox/) for Windows Defender Antivirus
- [x] [Only elevate](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings#user-account-control-only-elevate-executables-that-are-signed-and-validated) executables that are signed and validated

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/specify-cloud-protection-level-windows-defender-antivirus#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] [Configure](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-exploit-protection#windows-security-app) Exploit [Protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/exploit-protection)
- [ ] Microsoft [recommended block rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] UEFI Hardening (NSA Defensive Practices Guidance) [PDF](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf)
- [ ] Hardware and Firmware Security Guidance for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) & [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) - for other see the [overview](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance)
- [ ] Deploy [Windows Security Baselines](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-security-baselines) and keep it [up2date](https://www.microsoft.com/en-us/download/details.aspx?id=55319)

### For Enterprise/ Company only
- [ ] [Application Control](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control) (WDAC)
- [ ] [Enterprise Certificate Pinning](https://docs.microsoft.com/en-us/windows/access-protection/enterprise-certificate-pinning)
- [ ] [Block untrusted fonts in an enterprise](https://docs.microsoft.com/en-us/windows/threat-protection/block-untrusted-fonts-in-enterprise)
- [ ] [Web protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/web-protection-overview)
- [ ] [Protect](https://docs.microsoft.com/en-us/windows/security/identity-protection/remote-credential-guard) Remote Desktop credentials with Windows Defender Remote Credential Guard
- [ ] [Manage](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-manage-in-organization) Windows [Hello for Business](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-identity-verification)

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
* https://github.com/stoptracking/windows10
* https://github.com/frizb/Windows-Privilege-Escalation
* https://github.com/LOLBAS-Project/LOLBAS
* https://github.com/api0cradle/UltimateAppLockerByPassList
* https://trustedwindows.wordpress.com/
* https://docs.microsoft.com/en-us/windows-hardware/drivers/install/early-launch-antimalware
* https://www.microsoft.com/en-us/msrc/windows-security-servicing-criteria
* https://docs.microsoft.com/en-us/windows/security/threat-protection/overview-of-threat-mitigations-in-windows-10


<br />
All my commits are signed with my GPG Key:

ID 4AEE18F83AFDEB23 (0x620F071D)
<br />
Fingerprint: 3D3AA8EA763AA97DA252071497F9E213620F071D
