BackZip
=======
設定ファイルに指定されたファイルを、Zipファイルにバックアップする。  
設定ファイルには世代数が設定されていて、設定より古いバックアップは削除される。  
Zipファイルにはパスワードが設定できる。  
バックアップ時に動いていてはいけないプログラムを設定しておくと、
バックアップ開始前にチェックする。  

WindowsのHypertext Apprication（HTA）で実装。  
Zip圧縮にLhaplusが必要。  

バックアップ先のフォルダに設定ファイルを置く。  
**設定ファイルの例**  
	<?xml version="1.0" encoding="UTF-8" ?>
	<backup host="aitch2-VaioZ" user="aitch2-VaioZ\aitch2" rotate="5" passfile="C:\Becky!\backupkey.txt">
		<title>Becky! メール</title>
		<lhaplus path="C:\Program Files (x86)\Lhaplus\Lhaplus.exe"/>
		<process path="C:\Program Files (x86)\RimArts\B2\B2.exe" after="">Becky! Internet Mail 2</process>
		<source path="C:\Becky!">Becky! メール</source>
	</backup>


