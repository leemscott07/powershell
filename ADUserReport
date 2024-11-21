Import-Module ActiveDirectory
Get-ADUser ls066 -Properties enabled | select Name,enabled


Get-ADUser helpdesk -Properties * | Select UserPrincipalName

#Create UPN Report
Get-aduser -filter {mail -like "*"} -properties mail,userprincipalname | where-object {$_.userprincipalname -ne $_.mail -and $_.enabled -eq $true} | ft -AutoSize Name,UserPrincipalName,mail


Get-ADUser "AK030" -Properties msExchDelegateListLink | Select msExchDelegateListLink

Import-Csv -Path “C:\Temp\FleetAccountV2.csv” | ForEach-Object {Add-ADGroupMember -Identity “Fleet Portal Access Group-11007903871” -Members $_.'Username'}
