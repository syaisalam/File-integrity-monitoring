<h1>FIM - File Integrity Monitoring</h1>

<h2>Description</h2>
This project serves as a demonstration highlighting a fundamental aspect of security encapsulated within the CIA triad: integrity. Integrity in this context revolves around the trustworthiness and consistency of data. This implies that the original data remains unaltered; any unauthorized modifications will trigger an alert, signaling a breach in its integrity. To vividly illustrate this concept, a simple File Integrity Monitoring (FIM) application is developed. Essentially, this application oversees crucial files, affirming their integrity by cross-referencing the present state against a baseline. Notably, FIM are referenced as a pivotal security control within established frameworks and compliance protocols, including the PCI DSS (ID: W-06).

<h2>Languages</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="left">
The first part of the program allows two options for user input; option (A) requests new hashes for files whereas option (B) requests monitoring of existing files using a baseline previously created. For new files that has not been hashed, option A is recommended : <br/>
<img src="https://imgur.com/le5JTnM.png" height="45%" width="45%" alt="Disk Sanitization Steps]"/> 
<br />
<br />
If option A is selected, all files in the folder will be hashed using SHA-512 and saved as baseline.txt : <br/>
<img src="https://imgur.com/3wSdWE1.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
Baseline.txt will showcase the file path and the hash generated for each file : <br/>
<img src="https://i.imgur.com/U5IpYam.png" height="50%" width="60%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
If option B is selected, the program will start monitoring for changes in the folder every one second as long as the program is kept open :<br/>
<img src="https://i.imgur.com/xDrxSV1.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
The program cross-checks against the baseline for changes in the folder. It does this in three ways; (1) by checking for addition/creation of new files :  <br/>
<img src="https://i.imgur.com/dYotuSX.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
(2) by checking for compromise in the integrity of the file :  <br/>
<img src="https://i.imgur.com/pwVEwsO.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
(3) by checking for deletion of files :  <br/>
<img src="https://i.imgur.com/ZukwUr7.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
If any of the conditions are met, the program sends out alerts according to each of the condition, as shown below in green, yellow and red respectively :  <br/>
<img src="https://i.imgur.com/9xRzEzN.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
</p> 

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
