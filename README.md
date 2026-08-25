# cehpractical
Ceh practical notes

https://github.com/mzeeshanzafar28/CEH-Practical-CheatSheet 

https://github.com/infovault-Ytube/CEH-Practical-Notes

https://github.com/hunterxxx/CEH-v12-Practical

https://github.com/aniket2912/All-CEHv13-Module-wise-PDF-Reports

https://github.com/dhabaleshwar/CEHPractical/blob/main/Everything%20You%20Need.md

https://github.com/DarkLycn1976/CEH-Practical-Notes-and-Tools

$bytes = [System.IO.File]::ReadAllBytes("C:\Users\Administrator\Downloads\Conceal-Image-2025-01-14_gnp.exe")
$peOffset = [BitConverter]::ToInt32($bytes, 0x3C)
$magic = [BitConverter]::ToUInt16($bytes, $peOffset + 24)
Write-Host "Magic: 0x$($magic.ToString('X4'))"
$loaderFlags = [BitConverter]::ToUInt32($bytes, $peOffset + 24 + 88)
Write-Host "Loader Flags: 0x$($loaderFlags.ToString('X8'))"
