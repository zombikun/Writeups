# USB-Ripper
https://app.hackthebox.eu/challenges/usb-ripper

###### ダウンロード usbrip

`$ sudo -H python3 -m pip install -U usbrip`
( https://github.com/snovvcrash/usbrip )

###### usbripを使う

`# usbrip events violations auth.json --file syslog`

		[*] Started at 2021-10-10 17:25:21
	[17:25:23] [INFO] Reading "/home/cursed/Desktop/usb-ripper/syslog"
	100%|██████████████████████████████| 900000/900000 [00:16<00:00, 54268.58line/s]
	[17:25:40] [INFO] Opening authorized device list: "/home/cursed/Desktop/usb-ripper/auth.json"
	[17:25:40] [INFO] Searching for violations
	100%|██████████████████████████████| 100000/100000 [00:00<00:00, 545635.30dev/s]
	[?] How would you like your violation list to be generated?

    1. Terminal stdout
    2. JSON-file

	[>] Please enter the number of your choice (default 1): 2
	[>] Please enter the output file name (default is "viol.json"): weeb.json
	[17:26:23] [INFO] Generating violations list (JSON)
	[17:26:23] [INFO] New violations list: "/home/cursed/Desktop/usb-ripper/weeb.json"
	[*] Shut down at 2021-10-10 17:26:23
	[*] Time taken: 0:01:02.366472
  
  ###### ファイル.jsonを開く
  
	
	┌─[✗]─[root@oniichan]─[/home/cursed/Desktop/usb-ripper]
	└──╼ #open weeb.json
	Error: no "view" mailcap rules found for type "application/json"
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	Use of uninitialized value $file in open at /usr/share/perl5/File/MimeInfo/Applications.pm line 140.
	No applications found for mimetype: application/json
	.Running Firefox as root in a regular user's session is not supported.  ($XAUTHORITY is /home/cursed/.Xauthority which is owned by cursed.)
	Running Firefox as root in a regular user's session is not supported.  ($XAUTHORITY is /home/cursed/.Xauthority which is owned by cursed.)
	/usr/bin/open: 882: iceweasel: not found
	/usr/bin/open: 882: seamonkey: not found
	/usr/bin/open: 882: mozilla: not found
	/usr/bin/open: 882: epiphany: not found
	/usr/bin/open: 882: konqueror: not found
	/usr/bin/open: 882: chromium: not found
	/usr/bin/open: 882: chromium-browser: not found
	/usr/bin/open: 882: google-chrome: not found

                                                                               
	[                                                                              
    {                                                                          
        "conn": "????-08-03 07:18:01",
        "host": "kali",                                                        
        "vid": "3993",                                                         
        "pid": "9324",                                                         
        "prod": "1F8ADAEE73D993944FC7C7783",                                   
        "manufact": "884CCC9A3DF08F49C621373E",                                
        "serial": "71DF5A33EFFDEA5B1882C9FBDC1240C6",                          
        "port": "1-1",                                                         
        "disconn": "????-08-03 07:18:10"                                       
   	 }                                                                          
	]
  
###### シリアルmd5ハッシュを反転させれば完了です。
  
