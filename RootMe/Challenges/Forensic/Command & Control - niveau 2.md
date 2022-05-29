# コマンド＆コントロール - レベル2 
https://www.root-me.org/en/Challenges/Forensic/Command-Control-level-2

### "検証フラグはワークステーションのホスト名 "です。"

### そこで、"HOSTNAME "をgrepしても何も出てきません 

<img src=https://cdn.discordapp.com/attachments/932798167773220864/980515183258648656/unknown.png>

### 次に、USERNAMEを試してみました。

		cursed@oniichan:~/Desktop/Rootme/Forensics$ strings ch2.dmp | grep USERNAME
		USERNAME=John Doe
		USERNAME=WIN-ETSA91RKCFP$
		USERNAME=John Doe
		USERNAME=LOCAL SERVICE
		USERNAME=WIN-ETSA91RKCFP$
		USERNAME=John Doe
		USERNAME=WIN-ETSA91RKCFP$
    
### ワークステーションのホスト名はここです。以下はワークステーションのホスト名で、volatilityは使用していません。
