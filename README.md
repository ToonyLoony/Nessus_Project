<h1>Nessus Vulnerability Assessment Lab</h1>

<h2>Description</h2>
This project consists of peformning a simple vulnerability assessment on a virtual machine(LocalHost) using Nessus. Two types of scans were performed, the first being a basic scan with no credentials and another with user:pass credentails applied. In this project we are going to evaluate the differences between both scans, and look at factors such as additional vulnerabilities found
<br />

<h2>Utilities Used</h2>

- <b>Nessus</b> 

<h2>Environments Used </h2>

- <b>Windows 10(VM)</b> 

<h2>Project Walk-Through:</h2>

<p align="center">
  
<h3>Basic Scan(No credentials provided)</h3>


Launching Nessus: <br/>
<img src="" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Creating New Basic Scan:  <br/>
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
as you can see from the results.....



No Credentials Overview: <br/>
<img src="https://i.imgur.com/MIwnyWG.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />
Credentials Overview:  <br/>
<img src="https://i.imgur.com/lhv7gGA.png" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

Summary: from looking at both...

<h3> Remediation </h3>

In this section we will look to rectify some of the vulnerabilties listed


Uninstalling Firefox:  <br/>
<img src="" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

Performing Windows Updates:  <br/>
<img src="" height="80%" width="80%" alt="NessusLab"/>
<br />
<br />

</p>
