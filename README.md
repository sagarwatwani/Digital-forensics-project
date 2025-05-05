# Digital-forensics-project

Here's a README file template for your GitHub repository, detailing the forensic analysis, the findings, and the methodology used:


 Android Forensic Analysis Report

# Overview

This repository contains the detailed forensic analysis of an Android device (model LGMS330) that was extracted using chip-off forensics. The analysis aimed to investigate potential suspicious activity, unauthorized data harvesting, and other security concerns. The findings cover the device's system configuration, installed apps, root access status, and sensitive data storage, including a large volume of **credit card data* found during the investigation.



# Table of Contents

1. [Device Information](#device-information)
2. [Extraction Methodology](#extraction-methodology)
3. [Application Review](#application-review)
4. [Root Access / Kernel Integrity](#root-access--kernel-integrity)
5. [Browser History](#browser-history)
6. [Sensitive Data (Credit Cards)](#sensitive-data-credit-cards)
7. [File System & Orphan Files](#file-system--orphan-files)
8. [Additional Checks](#additional-checks)
9. [Overall Conclusion](#overall-conclusion)
    



# Device Information

 Manufacturer: LG Electronics
 Brand: MetroPCS
 Model: LGMS330 (LG K7)
 Device Codename: m1
 Chipset: Qualcomm Snapdragon 210 (msm8909)
 Android Version: 5.1.1 (Lollipop)
 Build ID: LMY47V
 Security Patch Level: 2015-12-01
 Factory Version: LGMS330AT-00-V10e-MPCS-US-DEC-23-2015-ARB00+0



# Extraction Methodology

The extraction was done using chip-off forensics—removing the memory chip for direct data access, bypassing the device’s operating system and security features. This ensures an unaltered, raw image of the device’s storage.



# Application Review

# Suspicious App Identified: HiddenMenu.apk

File Path: /img_Chipoff.001/vol_vol40/app/HiddenMenu/HiddenMenu.apk
Size: 3.2 MB
Hash (SHA-256): e27e63c839cdfe009b6174ee17be0fd6b0c86c7a254442c461f2ea24e9c3c656

The app appears to be a diagnostic or engineering tool. No evidence of spyware, exfiltration, or unauthorized data access was found. The app could be used in debugging or tampering scenarios.



# Root Access / Kernel Integrity

# Kernel Logs:

 Errors: Kernel stack corruption and decompression errors typically indicate reflashing or debugging activity.

No evidence of root access or tools like Magisk or SuperSU was found, suggesting that while the device may have been tampered with in the past, it currently has no active root access.



# Browser History

The device's browser history was benign with minimal activity, and no signs of malicious or harmful websites were identified. There were no phishing attempts or unauthorized access to personal accounts.



# Sensitive Data (Credit Cards)

# Critical Findings:

Folder Path: /img_Chipoff.001/vol_vol40/app/data/credit_cards/
Number of Files: 9,733 credit card records found in plaintext and image formats.

These files contained sensitive information, including card numbers, expiration dates, CVV codes, and images of the cards. No encryption or secure storage was used, making this a high-severity finding.



# File System & Orphan Files

Several *orphan files* were found with corrupted metadata, indicating past reflashing or system crashes. No malicious files or hidden data were discovered.



# Additional Checks

App Installation History: Nonuntrusted apps or malware found.
System Logs: No unauthorized access attempts were observed.
SMS/MMS Databases: Clean; no signs of command-and-control behavior.
Contacts & Call Logs: No suspicious activity.



# Overall Conclusion

# Key Findings:

Sensitive Data: A critical issue was the discovery of *9,733 credit card records* stored insecurely in plaintext and image formats, suggesting potential fraudulent activity.
HiddenMenu.apk: This app appears legitimate but may have been used in debugging scenarios.
Root Access: No active root access was detected; however, past tampering is evident.
Browser History: Benign; no malicious activity.
Orphan Files: Likely artifacts from reflashing or debugging, with no malicious content.







