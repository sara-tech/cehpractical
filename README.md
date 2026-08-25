# cehpractical
Ceh practical notes

https://github.com/mzeeshanzafar28/CEH-Practical-CheatSheet 

https://github.com/infovault-Ytube/CEH-Practical-Notes

https://github.com/hunterxxx/CEH-v12-Practical

https://github.com/aniket2912/All-CEHv13-Module-wise-PDF-Reports

https://github.com/dhabaleshwar/CEHPractical/blob/main/Everything%20You%20Need.md

https://github.com/DarkLycn1976/CEH-Practical-Notes-and-Tools

cd C:\Users\Administrator\Downloads
$bytes = [System.IO.File]::ReadAllBytes("Conceal-Image-2025-01-14_gnp.exe")
$peOffset = [BitConverter]::ToInt32($bytes, 0x3C)
$loaderFlags = [BitConverter]::ToUInt32($bytes, $peOffset + 24 + 88)
Write-Host "Loader Flags Value: 0x$($loaderFlags.ToString('X8'))"  
