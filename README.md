# Personal_Projects


#1
-
Tested in Wordpress version 4.2

This is the one we tested in the Lab of unit 7

[x]Turn on intercept in Burp </br>
[x]Upload new media </br>
[x]Catch in Burp and change file name to one with XSS inside </br>
[x]Once it's been uploaded to the website view image page </br>
[x]XSS will be executed. </br>
<img src="Assignment8-Exploit1.gif" alt="(XSS)">

#2
-
Tested in Wordpress version 4.2

[x] </br>
[x] </br>
[x] </br>
[x] </br>
[x] </br>

<img src="Assignment8-Exploit2.gif" alt=" (XSS)">

#3 Unauthenticated Stored Cross-Site Scripting (XSS)
-
Tested in Wordpress version 4.0

[x] </br>
[x] </br>
[x] </br>
[x] </br>
[x] </br>

<img src="Assignment8-Exploit3.gif" alt="Unauthenticated Stored Cross-Site Scripting (XSS)">

#4 Authenticated Shortcode Tags Cross-Site Scripting (XSS)
-
Tested in Wordpress version 4.0

[x] </br>
[x] </br>
[x] </br>
[x] </br>
[x] </br>

<img src="Assignment8-Exploit4.gif" alt="Authenticated Shortcode Tags Cross-Site Scripting (XSS)">

#5 Widgets Title Cross-Site Scripting (XSS)
-
Tested in Wordpress version 4.0

[x] </br>
[x] </br>
[x] </br>
[x] </br>
[x] </br>

<img src="Assignment8-Exploit5.gif" alt="Widgets Title Cross-Site Scripting (XSS)">

#6 Title: WordPress 2.9-4.7 - Authenticated Cross-Site scripting (XSS) in update-core.php
-
Summary : Multiple cross-site scripting (XSS) vulnerabilities in wp-admin/update-core.php in WordPress before 4.7.1 allow remote attackers to inject arbitrary web script or HTML via the (1) name or (2) version header of a plugin. </br>
Vulnerability type:XSS  </br>
CVE-ID:CVE-2017-5488  </br>
Tested in Wordpress version 4.7  </br>
Fixed in: 4.7.1  </br>

[x]Head to the plugins tab </br>
[x]Edit a plugin </br>
[x]change the name to some type of sscipt </br>
[x]Head to update tab (wp-admin/update-core.php) </br>
[x]Once it loads the script will run. </br>
</br>Affected code:<a href="https://github.com/WordPress/WordPress/blob/c9ea1de1441bb3bda133bf72d513ca9de66566c2/wp-admin/update-core.php">Source Code</a>
<img src="Assignment8-Exploit6.gif" alt="Authenticated Cross-Site scripting (XSS) in update-core.php">