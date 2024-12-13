🚨🚨 CVE-2024-53677-S2-067🚨🚨


Security Advisory: CVE-2024-53677 – Critical Apache Struts Remote Code Execution Vulnerability

Advisory Date: December 14, 2024

CVE ID: CVE-2024-53677

CVSS Score: 9.5 (Critical)

Overview

A critical vulnerability, CVE-2024-53677, has been identified in the popular Apache Struts framework, potentially allowing attackers to execute arbitrary code remotely. This vulnerability arises from flaws in the file upload logic, which can be exploited to perform path traversal and malicious file uploads.

The vulnerability impacts specific versions of Apache Struts and requires immediate attention from developers and administrators to mitigate the risk of exploitation.

Vulnerable Versions

The following versions of Apache Struts are affected:
2.0.0 to 2.5.33
6.0.0 to 6.3.0.2
The issue has been resolved in Apache Struts 6.4.0 and later versions

Description

CVE-2024-53677 is a critical vulnerability that allows attackers to exploit weaknesses in the file upload mechanism of Apache Struts. By manipulating the file upload parameters, an attacker can achieve the following:
Path Traversal: Upload files to arbitrary locations within the server, bypassing security mechanisms.
Remote Code Execution (RCE): Execute malicious code by uploading and triggering executable files, such as .jsp scripts or binary payloads.
According to the Apache Struts advisory, the vulnerability is not backward-compatible with older file upload mechanisms. As such, organizations using the deprecated file upload method must rewrite their actions to adopt the new, secure mechanism introduced in version 6.4.0.

Mitigation
1. Upgrade to Apache Struts 6.4.0 or Later
The Apache Struts team has resolved the vulnerability in version 6.4.0.
Migrate to the new Action File Upload Mechanism to ensure security. Note that this migration requires code refactoring due to non-backward compatibility.
S2-067 https://cwiki.apache.org/confluence/display/WW/S2-067
