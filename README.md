# cehpractical
Ceh practical notes

https://github.com/mzeeshanzafar28/CEH-Practical-CheatSheet 

https://github.com/infovault-Ytube/CEH-Practical-Notes

https://github.com/hunterxxx/CEH-v12-Practical

https://github.com/aniket2912/All-CEHv13-Module-wise-PDF-Reports

https://github.com/dhabaleshwar/CEHPractical/blob/main/Everything%20You%20Need.md

https://github.com/DarkLycn1976/CEH-Practical-Notes-and-Tools



# Check if there's more context
$bytes = [System.IO.File]::ReadAllBytes("C:\Users\Administrator\Downloads\Conceal-Image-2025-01-14_gnp.exe")
$peOffset = [BitConverter]::ToInt32($bytes, 0x3C)
# Check all optional header fields
$optionalHeader = $peOffset + 24
Write-Host "NumberOfRvaAndSizes: $([BitConverter]::ToUInt32($bytes, $optionalHeader + 92).ToString('X8'))"
Write-Host "LoaderFlags: $([BitConverter]::ToUInt32($bytes, $optionalHeader + 88).ToString('X8'))"
