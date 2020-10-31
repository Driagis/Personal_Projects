
#1 Title: WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
-
This is the one we tested in the Lab of unit 7 </br>
Summary : Cross-site scripting (XSS) vulnerability in the media_handle_upload function in wp-admin/includes/media.php in WordPress before 4.6.1 might allow remote attackers to inject arbitrary web script or HTML by tricking an administrator into uploading an image file that has a crafted filename. </br>
Vulnerability type:XSS  </br>
CVE-ID: CVE-2016-7168 </br>
Version: Tested in Wordpress version 4.2 </br>
Fixed in: 4.6.1  </br>

[x]Turn on intercept in Burp </br>
[x]Upload new media </br>
[x]Catch in Burp and change file name to one with XSS inside </br>
[x]Once it's been uploaded to the website view image page </br>
[x]XSS will be executed. </br>
<img src="Assignment8-Exploit1.gif" alt="(XSS)">
</br>Affected code:<a href="https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0">Source Code</a> </br>
#2 Title: WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
-
Tested in Wordpress version 4.2
Summary : WordPress before 4.2.3 does not properly verify the edit_posts capability, which allows remote authenticated users to bypass intended access restrictions and create drafts by leveraging the Subscriber role, as demonstrated by a post-quickdraft-save action to wp-admin/post.php. </br>
Vulnerability type:XSS  </br>
CVE-ID: CVE-2015-5623 </br>
Version: Tested in Wordpress version 4.2 </br>
Fixed in: 4.2.3  </br>

[x]Head to the pages tab </br>
[x]Edit the page's text instead of the visual part. </br>
[x] Update the page</br>
[x]Load the page that was edited </br>
[x]Once the action is done the script will execute. (This one used on onmouseover) </br>

<img src="Assignment8-Exploit2.gif" alt=" (XSS)">

#3 Title: WordPress <= 4.1.1 - Unauthenticated Stored Cross-Site Scripting (XSS)
-
Summary : Multiple cross-site scripting (XSS) vulnerabilities in WordPress before 4.1.2, when MySQL is used without strict mode, allow remote attackers to inject arbitrary web script or HTML via a (1) four-byte UTF-8 character or (2) invalid character that reaches the database layer, as demonstrated by a crafted character in a comment. </br>
Vulnerability type:XSS  </br>
CVE-ID: CVE-2015-3438 </br>
Version: Tested in Wordpress version 4.0 </br>
Fixed in: 4.1.2 </br>
In this one there was 2 ways to do it. After not being able to get the first way to wrok properly I then tried the second way. Which inserts the script into the content of the comments instead of the author line. Both ways could be shown here https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/

[x]Load up http://wpdistillery.vm/ without logging in </br>
[x] Enter the required information into the fields </br>
[x] Inside the comment content add some random text and create a new line (press enter) insert the script inside a block qoute with the crafter character</br>
[x] submit the comment</br>
[x] Once the action is done the script will run. (this one used onmouseover) </br>

<img src="Assignment8-Exploit3.gif" alt="Unauthenticated Stored Cross-Site Scripting (XSS)">

#4 Title: WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
-
Summary : Cross-site scripting (XSS) vulnerability in WordPress before 4.3.1 allows remote attackers to inject arbitrary web script or HTML by leveraging the mishandling of unclosed HTML elements during processing of shortcode tags. </br>
Vulnerability type:XSS  </br>
CVE-ID: CVE-2015-5714 </br>
Version: Tested in Wordpress version 4.0 </br>
Fixed in: 4.3.1  </br>

[x]Head to the pages/posts tab </br>
[x]Create a new page/post or edit an existing page/post </br>
[x]Insert the shortcode with script inside </br>
[x]Load affected page/post</br>
[x]Script will be executed depending on the script (this one works on load) </br>
</br>Affected code:<a href="https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8">Source Code</a> </br>
<img src="Assignment8-Exploit4.gif" alt="Authenticated Shortcode Tags Cross-Site Scripting (XSS)">

#5 Title: WordPress <= 4.2.3 - Widgets Title Cross-Site Scripting (XSS)
-
Summary: Cross-site scripting (XSS) vulnerability in the form function in the WP_Nav_Menu_Widget class in wp-includes/default-widgets.php in WordPress before 4.2.4 allows remote attackers to inject arbitrary web script or HTML via a widget title.  </br>
Vulnerability type: XSS  </br>
CVE-ID: CVE-2015-5732 </br>
Version: Tested in Wordpress version 4.0 </br>
Fixed in: 4.2.4  </br>

[x]Head to appearcnce tab and select widget </br>
[x]Add a text widget </br>
[x]Add anything into the title </br>
[x]Write script into the paragraph of the widget </br>
[x]Load page and the script executes </br>
</br>Affected code:<a href="https://core.trac.wordpress.org/changeset/33529">Source Code</a> </br>
<img src="Assignment8-Exploit5.gif" alt="Widgets Title Cross-Site Scripting (XSS)">

#6 Title: WordPress 2.9-4.7 - Authenticated Cross-Site scripting (XSS) in update-core.php
-
Summary : Multiple cross-site scripting (XSS) vulnerabilities in wp-admin/update-core.php in WordPress before 4.7.1 allow remote attackers to inject arbitrary web script or HTML via the (1) name or (2) version header of a plugin. </br>
Vulnerability type:XSS  </br>
CVE-ID:CVE-2017-5488  </br>
Version: Tested in Wordpress version 4.7  </br>
Fixed in: 4.7.1  </br>

[x]Head to the plugins tab </br>
[x]Edit a plugin </br>
[x]change the name to some type of sscipt </br>
[x]Head to update tab (wp-admin/update-core.php) </br>
[x]Once it loads the script will run. </br>
</br>Affected code:<a href="https://github.com/WordPress/WordPress/blob/c9ea1de1441bb3bda133bf72d513ca9de66566c2/wp-admin/update-core.php">Source Code</a> </br>
<img src="Assignment8-Exploit6.gif" alt="Authenticated Cross-Site scripting (XSS) in update-core.php">
