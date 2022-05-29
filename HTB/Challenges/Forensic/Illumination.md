# Illumination / イルミネーション
https://app.hackthebox.eu/challenges/87

###### zipを展開する

###### .gitという名前のディレクトリが見えます。

		┌─[cursed@oniichan]─[~/Desktop]
		└──╼ $ls -la
		total 44
		drwxr-xr-x 1 cursed cursed   140 10 oct.  22:43 .
		drwxr-xr-x 1 cursed cursed   512 10 oct.  16:50 ..
		drwx------ 1 cursed cursed   146 30 mai    2019 .git
		drwx------ 1 cursed cursed    42 10 oct.  22:44 Illumination.JS
		-rw-r--r-- 1 cursed cursed 38054 10 oct.  22:36 Illumination.zip
		-rw-r--r-- 1 cursed cursed  2220 14 avril 00:08 README.license
		drwxr-xr-x 1 cursed cursed    56 10 oct.  17:10 sterraxcyl
				drwxr-xr-x 1 cursed cursed    48 10 oct.  17:26 usb-ripper
		drwxr-xr-x 1 cursed cursed     0  9 oct.  19:50 y
   
###### .gitディレクトリに移動します。

		┌─[cursed@oniichan]─[~/Desktop/.git]
		└──╼ $ls -la
		total 24
		drwx------ 1 cursed cursed 146 30 mai    2019 .
		rwxr-xr-x 1 cursed cursed 140 10 oct.  22:43 ..
		-rw-r--r-- 1 cursed cursed 795 30 mai    2019 COMMIT_EDITMSG
		-rw-r--r-- 1 cursed cursed 130 30 mai    2019 config
		-rw-r--r-- 1 cursed cursed  73 30 mai    2019 description
		-rw-r--r-- 1 cursed cursed  23 30 mai    2019 HEAD
		drwx------ 1 cursed cursed 414 30 mai    2019 hooks
		-rw-r--r-- 1 cursed cursed 217 30 mai    2019 index
		drwx------ 1 cursed cursed  14 30 mai    2019 info
		drwx------ 1 cursed cursed  16 30 mai    2019 logs
		drwx------ 1 cursed cursed 116 30 mai    2019 objects
		-rw-r--r-- 1 cursed cursed  41 30 mai    2019 ORIG_HEAD
		drwx------ 1 cursed cursed  18 30 mai    2019 refs
    
###### ログを見ることができます

		┌─[✗]─[cursed@oniichan]─[~/Desktop/.git]
		└──╼ $git log
		commit edc5aabf933f6bb161ceca6cf7d0d2160ce333ec (HEAD -> master)
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 14:16:43 2019 +0100

    Added some whitespace for readability!

		commit 47241a47f62ada864ec74bd6dedc4d33f4374699
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 12:00:54 2019 +0100

    Thanks to contributors, I removed the unique token as it was a security risk. Thanks for reporting responsibly!

		commit ddc606f8fa05c363ea4de20f31834e97dd527381
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 09:14:04 2019 +0100

    Added some more comments for the lovely contributors! Thanks for helping out!

		commit 335d6cfe3cdc25b89cae81c50ffb957b86bf5a4a
		Author: SherlockSec <dan@lights.htb>
		Date:   Thu May 30 22:16:02 2019 +0100
		:...skipping...
		commit edc5aabf933f6bb161ceca6cf7d0d2160ce333ec (HEAD -> master)
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 14:16:43 2019 +0100

    Added some whitespace for readability!

		commit 47241a47f62ada864ec74bd6dedc4d33f4374699
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 12:00:54 2019 +0100

    Thanks to contributors, I removed the unique token as it was a security risk. Thanks for reporting responsibly!

		commit ddc606f8fa05c363ea4de20f31834e97dd527381
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 09:14:04 2019 +0100

    Added some more comments for the lovely contributors! Thanks for helping out!

		commit 335d6cfe3cdc25b89cae81c50ffb957b86bf5a4a
		Author: SherlockSec <dan@lights.htb>
		Date:   Thu May 30 22:16:02 2019 +0100

    Moving to Git, first time using it. First Commit!
		~
		~
		~
		~
		~
		~
  
###### 私たちはトークンを見つけなければならないことを忘れないでください。:

	┌─[cursed@oniichan]─[~/Desktop/.git]
		└──╼ $git show 47241a47f62ada864ec74bd6dedc4d33f4374699
		commit 47241a47f62ada864ec74bd6dedc4d33f4374699
		Author: SherlockSec <dan@lights.htb>
		Date:   Fri May 31 12:00:54 2019 +0100

    Thanks to contributors, I removed the unique token as it was a security risk. Thanks for reporting responsibly!

		diff --git a/config.json b/config.json
		index 316dc21..6735aa6 100644
		--- a/config.json
		+++ b/config.json
		@@ -1,6 +1,6 @@
		 {
 
		-       "token": "SFR*****************************************",
		+       "token": "Replace me with token when in use! Security Risk!",
    				"prefix": "~",
		        "lightNum": "1337",
 		       "username": "UmVkIEhlcnJpbmcsIHJlYWQgdGhlIEpTIGNhcmVmdWxseQ==",
           
###### 最後に、トークンがあります。デコードする必要があります。
