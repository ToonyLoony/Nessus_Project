<h1>Nessus Vulnerability Assessment Lab</h1>

<h2>Description</h2>
This project consists of peformning a simple vulnerability assessment on a virtual machine(LocalHost) using Nessus. Two types of scans were performed, the first being a basic scan with no credentials and another with user:pass credentails applied. In this project we are going to evaluate the differences between both scans and then remediate the vulnerabilities
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

As you can see As you can see As you can see As you can see As you can see As you can see As you can see 


<br />

<h3>Scan with Credentials Provided</h3>

Next, we want to do a credential scan. To perform this we must do a few prerequisites first. To perform a credential scan for windows hosts not on the domain, we must allow 'remote registry' on the windows services. This will allow nessus to connect to the windows remote registry and crawl through the registry for any vulnerabilities


Inputing User Credentials:  <br/>
<img src="https://i.imgur.com/EeuTNCq.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Allowing Remote Registry:  <br/>
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
<br />
No Credentials Overview: <br/>
<img src="https://i.imgur.com/MIwnyWG.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Credentials Overview:  <br/>
<img src="https://i.imgur.com/lhv7gGA.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

<h3> Remediation </h3>

In this section we will look to rectify some of the vulnerabilties listed


Uninstalling Firefox:  <br/>
<img src="https://i.imgur.com/KYhDm65.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

Performing Windows Updates:  <br/>
<img src="https://i.imgur.com/BsjbPU8.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
<br />
<h3>Scan with Credentials Provided</h3>
<br />
<br />
Conclusion:  <br/>
<img src="https://i.imgur.com/jQPIxve.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
<br />
After updating windows and uninstalling firefox we see a significant drop in the amount of vulnerabilties present. Oringinally we had '73' critical and '81' high severity vulnerabilties, now after just running a windows updates once and uninstalling firefox we have '0' critical and '7' high vulnerabilities. Although this is an excellent drop in the amount of vulnerabilties, what is still present is still very danagerous. What can see that the '7' high severity vulnerablties are susseptible to 'RCE' attacks. As we all know remote code execution is no joke and should be rectified ASAP.

Overall this was just a very short demonstration of me using Nessus, i hope you learnt something and enjoyed :p 
</p>
