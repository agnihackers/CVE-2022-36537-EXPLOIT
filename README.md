# CVE-2022-36537

# Summary

R1Soft Server Backup Manager uses the ZK framework as the main framework. Its security requires all Web3 project parties to pay more attention to the security vulnerabilities of various Web3 infrastructures and patch them in time to avoid potential security risks and digital asset losses. We will dig out in time, track various security risks on web3, and provide leading security solutions to ensure that the web3 world chain and off-chain are safe and sound.

# Preface

ZK is the leading open-source Java Web framework for building enterprise Web applications. With over 2,000,000 downloads, ZK empowers a wide variety of companies and institutions, ranging from small to Fortune Global 500 in multiple industries.

R1Soft Server Backup Manager (SBM) offers service providers a flexible, server-friendly solution that takes the hassle out of running traditional backups. Users can run backups every 15 minutes without impacting server performance. Nearly 1,800 service providers use it to protect 250,000 servers.

# Affected Versions

ZK Framework `v9.6.1, 9.6.0.1, 9.5.1.3, 9.0.1.2 and 8.6.4.1.`

ConnectWise Recover `v2.9.7` and earlier versions are impacted.

R1Soft Server Backup Manager `v6.16.3` and earlier versions are impacted.

# ZK Framework Auth Bypass

![ZK](https://raw.githubusercontent.com/agnihackers/CVE-2022-36537-EXPLOIT-TOOL/main/unnamed.png)
![ZK-5150](https://raw.githubusercontent.com/agnihackers/CVE-2022-36537-EXPLOIT-TOOL/main/ZK-5150.png)

From the vulnerability description, if the route /zkau/upload contains the nextURI parameter, the ZK AuUploader servlet will forward the forward request, which can bypass the identity authentication and return the files in the web context, such as obtaining web.xml, zk page, applicationContext -security.xml configuration information, etc.

# Install

`You need python3, pip3, git.`
```
git clone https://github.com/agnihackers/CVE-2022-36537-EXPLOIT.git
cd CVE-2022-36537-EXPLOIT
pip3 install -r requirements.txt
chmod +x mysql-connector-java-5.1.48.jar
python3 CVE-2022-36537.py
```

# Shodan Dork 

![shodan](https://raw.githubusercontent.com/agnihackers/CVE-2022-36537-EXPLOIT-TOOL/main/Shodan%20Dork.jpg)

# CVE-2022–36537 Vulnerability More Details 

https://twitter.com/AGNIHACKERS1/status/1601162549084696579?s=20&t=ncMMG7XNNZDns4Wn5CfPoA
