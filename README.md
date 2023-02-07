<h1>System Update and Upgrade</h1>

<h2>Description</h2>
Project consists using the APT package manager to update the repository database and repository links.
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b>
- <b>Debian Environment</b>
- <b>Terminal</b>

<h2>Reviewing Repository Types:</h2>
The terminal is opened and the root user is accessed:<br/>
<img src="https://imagizer.imageshack.com/img924/256/5Q85PR.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The sources.list file is opened with nano:<br/>
<img src="https://imagizer.imageshack.com/img924/8443/waYUtp.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The Debian website is checked to review the different types of repositories for Debian versions:<br/>
<img src="https://imagizer.imageshack.com/img922/6357/UnaCXs.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The packet under Debian 10.4 is confirmed as Buster, and the outsources list is closed:<br/>
<img src="https://imagizer.imageshack.com/img924/2295/xRgDOX.png" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Updating & Adding a Repository:</h2>
The apt update command is used to update the database of available packages:<br/>
<img src="https://imagizer.imageshack.com/img924/3114/6qoUac.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The nano command is used to add the required sources.list repository:<br/>
<img src="https://imagizer.imageshack.com/img924/4886/hljA1p.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The following line is added to the repository: deb http://http.kali.org/kali kali-rolling main contrib non-free: The apt update command is then used to reach out to the website to pull updates:<br/>
<img src="https://imagizer.imageshack.com/img924/7646/aGINmp.png" alt="Disk Sanitization Steps"/>
<br />
<br />
After running apt update, it can be noted that there was an issue with the public key used for this distribution:<br/>
<img src="https://imagizer.imageshack.com/img923/7014/EdQcg7.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Within the home directory, the following command is used to download the require key: apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-
keys ED444FF07D8D0BF6:<br/>
<img src="https://imagizer.imageshack.com/img923/2504/3FbrgI.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The command apt update is then used successfuly to update the database of available packages:<br/>
<img src="https://imagizer.imageshack.com/img922/9977/Ox9G1J.png" alt="Disk Sanitization Steps"/>
<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
