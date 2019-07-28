## Make-Certificate

makecert /n "CN=NameOfProject" /r /pe /a sha512 /len 4096 /cy authority /sv "D:\User\Desktop\Name Of Project.pvk" "D:\User\Desktop\Name Of Project.cer"

pvk2pfx -pvk "D:\User\Desktop\Name Of Project.pvk" -spc "D:\User\Desktop\Name Of Project.cer" -pfx "D:\User\Desktop\Name Of Project.pfx" -pi superrrSecretePass

Certutil -addStore TrustedPeople "D:\User\Desktop\Name Of Project.cer"

Certutil -store TrustedPeople

## Requirements
[Windows Development Kit](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk)