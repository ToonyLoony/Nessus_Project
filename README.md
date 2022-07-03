<h1>Nessus Vulnerability Assessment Lab</h1>

<h2>Description</h2>
This project consists of performing a simple vulnerability assessment on a virtual machine(LocalHost) using Nessus. Two types of scans were performed, the first being a basic scan with no credentials and another with user:pass credentials applied. In this project, we are going to evaluate the differences between both scans and then remediate the vulnerabilities
<br />

<h2>Utilities Used</h2>

- <b>Nessus</b> 

<h2>Environments Used </h2>

- <b>Windows 10(VM)</b> 

<h2>Project Walk-Through</h2>

<p align="center">
  
<h3>Basic Scan(No credentials provided)</h3>

Launching Nessus: <br/>
<img src="https://i.imgur.com/8ImLRft.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Creating our first Scan:  <br/>
<img src="https://i.imgur.com/p8taT2F.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Scan Results: <br/>
<img src="https://i.imgur.com/rgZ4XMh.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

<h3>Scan with Credentials Provided</h3>

Next, we will perform a credential scan, however, before doing this we must ensure the 'remote registry' service is enabled. This will allow Nessus to connect to the windows remote registry and crawl through the registry for any vulnerabilities


Inputing User Credentials:  <br/>
<img src="https://i.imgur.com/EeuTNCq.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Enabling Remote Registry Service:  <br/>
<img src="https://i.imgur.com/X3wbYFp.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Assessment Results:  <br/>
<img src="https://i.imgur.com/cJv3cSx.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

<h3> Credentials VS No Credentials </h3>
<br />
<br />
<br />
No Credentials Assessment Overview: <br/>
<img src="https://i.imgur.com/MIwnyWG.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Credentials Assessment Overview:  <br/>
<img src="https://i.imgur.com/lhv7gGA.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
As conveyed above, we're able to identify a plethora of vulnerabilities once we opt to use the credential scan. This is because when the remote registry is enabled we're able to look at things such as the file system registry and running services, thus making it a much more in-depth and extensive scan.


In the upcoming section, i will look to remediate some of the vulnerabilities found in the latest scan(cred scan) 

<h3> Remediation </h3>

In this section, we will look to rectify some of the vulnerabilities found

Uninstalling Firefox:  <br/>
<img src="https://i.imgur.com/KYhDm65.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

Performing Windows Updates:  <br/>
<img src="https://i.imgur.com/BsjbPU8.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />


<h3>Follow up scan after performing remediation</h3>
<br />
<br />
<img src="https://i.imgur.com/jQPIxve.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
<h4>Conclusion</h4>
After updating windows and uninstalling firefox we see a significant drop in the number of vulnerabilities present. Originally we had '73' critical and '81' high severity vulnerabilities, now after just running a windows update once and uninstalling firefox we have '0' critical and '7' high vulnerabilities. Although this is an excellent drop in the number of vulnerabilities, what is still present is very dangerous. This is because the '7' high severity vulnerabilities are susceptible to 'RCE' attacks. As we all know remote code execution is no joke and should be rectified ASAP. To remediate these vulnerabilities, more updates should be applied, whilst also doing follow-up research on the CVEs that are present.

Overall this was just a very short demonstration of me using Nessus, I hope you learned something and enjoyed :p 
</p>
