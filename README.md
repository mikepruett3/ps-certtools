# PowerShell Certificate Tools (ps-certtools)

Module create to include custom functions that work with Certificates. For use with other cmdlets and scripts.

## Installation

Clone the repository into your **$Home\Documents\WindowsPowerShell\Modules** folder (create the Modules folder if you dont have one already)

```powershell
cd $env:UserProfile\Documents\WindowsPowerShell\Modules\
git clone https://github.com/mikepruett3/ps-certtools.git
```

Then you can import the custom module into your running shell...

```powershell
Import-Module ps-certtools
```

## Usage

### Convert-PFX2PEM

Use this function to create the appropriate ASCII encoded Certificate files. This includes the following files:

- A CA Certificate bundle file
- A separate Public Certificate file
- A separate DER-Encoded file
- A separate Private Key file
- A separate PEM-Encoded file

Example

```PowerShell
> Convert-PFX2PEM -Path "c:\example.pfx" -Passphrase "mypassword"
```

Will result in the following files generated:

- C:\example.chain.cer
- C:\example.crt
- C:\example.der
- C:\example.key
- C:\example.pem
