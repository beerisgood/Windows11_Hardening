!**Work in progress / rebuild<br />
Any help is welcome**!
<br />

# Requirements
- [x] Always use latest [Windows 10 stable version](https://www.microsoft.com/en-us/software-download/windows10)
- [x] Always keep your System [up2date](https://support.microsoft.com/en-gb/help/4027667/windows-10-update)
- [x] Use (default activated) internal Windows Defender protection instead of external "Security" solutions
- [x] Check regular for new Driver and Program updates **&** install them
- [x] Avoid any "Tuning" tools
- [x] Only use/ install tools which you realy need
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#requirements-met-by-system-guard-enabled-machines) for [System Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows) / [Hardware-based Isolation](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/overview-hardware-based-isolation)
- [x] [Hardware Requirements](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/requirements-and-deployment-planning-guidelines-for-virtualization-based-protection-of-code-integrity#baseline-protections) for [Memory integrity](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/memory-integrity)

<br />

## Hardening
- [x] Deploy latest [Microsoft Security Baseline](https://www.microsoft.com/en-us/download/details.aspx?id=55319) and keep it up2date
- [x] Install [Windows Defender Application Guard](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-guard/install-wd-app-guard#install-application-guard) (WDAG)
- [x] Enable [network protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection#powershell)
- [x] Enable [controlled folder access](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-controlled-folders#powershell)
- [x] Enable [attack surface reduction rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#powershell) (ASR)
- [x] Enable [System Guard Secure Launch](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-system-guard/system-guard-secure-launch-and-smm-protection#windows-security-center)
- [x] Enable [cloud-delivered protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/enable-cloud-protection-windows-defender-antivirus)
- [x] [Configure PUA protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection) in Windows Defender Antivirus
- [x] Enable [Bitlocker Encryption](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-device-encryption-overview-windows-10)

<br />

### Further Hardening
- [ ] Specify the [cloud-delivered protection level](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/specify-cloud-protection-level-windows-defender-antivirus#use-group-policy-to-specify-the-level-of-cloud-delivered-protection)
- [ ] Configure [exploit protection](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-exploit-protection#windows-security-app)
- [ ] Control [USB devices and other removable media](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-control/control-usb-devices-using-intune)
- [ ] UEFI Hardening (NSA Defensive Practices Guidance) [PDF](https://www.nsa.gov/Portals/70/documents/what-we-do/cybersecurity/professional-resources/ctr-uefi-defensive-practices-guidance.pdf)
- [ ] Hardware and Firmware Security Guidance for [Windows](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#win) & [AMD CPUs](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance#54-amd) - for other see the [overview](https://github.com/nsacyber/Hardware-and-Firmware-Security-Guidance/tree/master/guidance)

### For Enterprise/ Company only
- [ ] Configure [Application Control](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control)

<br />

###### Test Config
- https://demo.wd.microsoft.com/
- [Validate connections](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-network-connections-windows-defender-antivirus#validate-connections-between-your-network-and-the-cloud) between your network and the Windows Defender Antivirus cloud service
- [Validate](https://techcommunity.microsoft.com/t5/Microsoft-Defender-ATP/Tamper-protection-now-generally-available-for-Microsoft-Defender/ba-p/911482) Windows Defender Tamper protection
- Windows Defender SmartScreen [Demo Pages](https://demo.smartscreen.msft.net/)

<br />

###### Read stuff:

Needed Windows Defender Connections: https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-network-connections-windows-defender-antivirus & https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/configure-proxy-internet#verify-client-connectivity-to-microsoft-defender-atp-service-urls

Take a look at this awesome tools: https://github.com/AndyFul/Hard_Configurator & https://github.com/securitywithoutborders/hardentools

Not realy hardening related stuff:
https://github.com/frizb/Windows-Privilege-Escalation & https://www.absolomb.com/2018-01-26-Windows-Privilege-Escalation-Guide/

<br />
All my commits are signed with my GPG Key:

ID 4AEE18F83AFDEB23 (0x620F071D)
<br />
Fingerprint: 3D3AA8EA763AA97DA252071497F9E213620F071D
