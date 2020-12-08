# ArchersHandbook
All the things I know...

## MSBuildShell - Get all the Powershells
No Powershell?  No problem!
1. Get [MSBuildShell script](https://github.com/Cn33liz/MSBuildShell/blob/master/MSBuildShell.csproj)
2. Use Microsoft binary MSBuild.exe to run the script `MSBuild.exe MSBuildShell.csproj`
3. Get the PS shellz
![alt text](https://github.com/4rch3r23/ArchersHandbook/blob/main/Screen%20Shot%202020-11-10%20at%201.26.47%20PM.png)

## Windows Host Enumeration

##### WinPEAs
- [WinPEAs Exe](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS/winPEASexe)
- [WinPEAs Bat](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS/winPEASbat)

##### PrivescCheck.ps1
- [PrivescCheck.ps1 (Based on PowerUp)](https://github.com/itm4n/PrivescCheck)
###### Basic usage

From a command prompt:
```
C:\Temp\>powershell -ep bypass -c ". .\PrivescCheck.ps1; Invoke-PrivescCheck"
```

From a PowerShell prompt:
```
PS C:\Temp\> Set-ExecutionPolicy Bypass -Scope process -Force
PS C:\Temp\> . .\PrivescCheck.ps1; Invoke-PrivescCheck
```

###### Extended mode

By default, the scope is limited to __vulnerability discovery__ but, you can get a lot more information with the `-Extended` option:

From a command prompt:
```
C:\Temp\>powershell -ep bypass -c ". .\PrivescCheck.ps1; Invoke-PrivescCheck -Extended"
```

From a PowerShell prompt:
```
PS C:\Temp\> Set-ExecutionPolicy Bypass -Scope process -Force
PS C:\Temp\> . .\PrivescCheck.ps1; Invoke-PrivescCheck -Extended
```

## Obfusctate files for movement / hiding
###### Will create compressed version of desired file that is also Base64 encoded
```
certutil -encode .\InFile .\OutfileB64 && tar -cvf compressedFile .\OutfileB64
```
You can also replace `-encode` with `-encodehex` to alternatively (or in addition to) HEX encode your file.

###### For Extracting obfuscated file
```
tar -xvf .\compressedFile && certutil -decode .\OutfileB64 .\InFile
```

## All the Payloads!
[PAYLOADS](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/7f36bf58a4dafaa6749a2af3f8d422f15c00f35e/Server%20Side%20Template%20Injection/README.md)
