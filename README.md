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

# If Magic is 0x10B (32-bit), LoaderFlags is at +68
# If Magic is 0x20B (64-bit), LoaderFlags is at +88

# Try BOTH offsets:
$loaderFlags32 = [BitConverter]::ToUInt32($bytes, $peOffset + 24 + 68)
$loaderFlags64 = [BitConverter]::ToUInt32($bytes, $peOffset + 24 + 88)
Write-Host "32-bit Loader Flags: 0x$($loaderFlags32.ToString('X8'))"
Write-Host "64-bit Loader Flags: 0x$($loaderFlags64.ToString('X8'))"
