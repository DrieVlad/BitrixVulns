Exploitation of vulnerabilities requires access with administrator privileges.

## CVE-2024-34887 (BDU:2024-08600)

[BDU:2024-08600](https://bdu.fstec.ru/vul/2024-08600)

A remote attacker can abuse the "Check Connection" button in the AD/LDAP module settings. When changing the parameters of a specific server, an IP address controlled by the attacker can be entered. As a result, the AD domain administrator password will be obtained in clear text.

Insufficiently protected credentials in AD/LDAP server settings in 1C-Bitrix Bitrix24 23.300.100 allows remote administrators to cause sending AD/LDAP administrators accounts passwords to arbitrary server via HTTP POST request.

### Explotation:
1. Go to the AD/LDAP module settings.
2. Select the desired server and click "Change server settings".
3. Change the server address in the "Server:port:" field to the IP address controlled by the attacker.
4. Click the "Check connection" button.

As a result, the AD domain administrator credentials will be obtained in clear text.

CVSS v3: (AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:N/A:N)

Base Score: 6.8

## CVE-2024-34882 (BDU:2024-08612)

[BDU:2024-08612](https://bdu.fstec.ru/vul/2024-08612)

A remote attacker can abuse SMTP settings and obtain the SMTP password in clear text.

Insufficiently protected credentials in SMTP server settings in 1C-Bitrix Bitrix24 23.300.100 allows remote administrators to send SMTP account passwords to an arbitrary server via HTTP POST request.

### Explotation:

1. In the "Administration" section, go to SMTP settings.
2. Select the desired server and click "Change".
3. Using developer tools, open the page's source code.
4. Find the table cell "password".

As a result, you will receive the SMTP password in clear text.

CVSS v3: (AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:N/A:N)

Base Score: 6.8

## CVE-2024-34883 (BDU:2024-08613)

[BDU:2024-08613](https://bdu.fstec.ru/vul/2024-08613)

A remote attacker can abuse the DAV module settings and obtain the proxy server password in clear text.

Insufficiently protected credentials in DAV server settings in 1C-Bitrix Bitrix24 23.300.100 allow remote administrators to read proxy-server accounts passwords via HTTP GET request.

### Explotation:
1. In the "Administration" section, go to the DAV module settings.
2. Go to the "Proxy" section.
3. Using developer tools, open the page's source code.
4. Find the table cell "proxy_password".

As a result, the credentials from the proxy server will be received in clear text.

CVSS v3: (AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:N/A:N)

Base Score: 6.8

## CVE-2024-34885 (BDU:2024-08610)

[BDU:2024-08610](https://bdu.fstec.ru/vul/2024-08610)

A remote attacker can abuse the "Apply" button in the "SMTP Settings" section. In changing the parameters of a specific server, an IP address controlled by the attacker can be entered. As a result, the SMTP password will be obtained in base64 format.

Insufficiently protected credentials in SMTP server settings in 1C-Bitrix Bitrix24 23.300.100 allows remote administrators to read SMTP accounts passwords via HTTP GET request.

### Explotation:

1. In the "Administration" section, go to SMTP settings.
2. Select the desired server and click "Change".
3. Change the server address in the "Server" field to an IP address controlled by the attacker.
4. Click the "Apply" button.

As a result, you will receive the password from SMTP in base64 format.

CVSS v3: (AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:N/A:N)

Base Score: 6.8

## CVE-2024-34891 (BDU:2024-08611)

[BDU:2024-08611](https://bdu.fstec.ru/vul/2024-08611)

A remote attacker can abuse the DAV module settings and obtain the Exchange server password in clear text.

Insufficiently protected credentials in DAV server settings in 1C-Bitrix Bitrix24 23.300.100 allows remote administrators to read Exchange account passwords via HTTP GET request.

### Explotation:
1. In the "Administration" section, go to the DAV module settings.
2. Using developer tools, open the page's source code.
3. Find the table cell "exchange_password".

As a result, the credentials from the Exchange server will be received in clear text.

CVSS v3: (AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:N/A:N)

Base Score: 6.8

## Remediation

There is currently no fix. It is recommended to use least privilege credentials. It is also recommended to differentiate access rights based on the role model.

Discoverer: **Vladislav Driev, Oleg Labyntsev** 

Contacts: [GigaHackers](https://t.me/GigaHack)
