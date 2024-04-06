## oh-my-posh-window-guide

 - install [winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)
 - install Nerd Fonts: [nerd-fonts](https://github.com/ryanoasis/nerd-fonts/) (to get icons ,dont worries you can still use your favorite font if they are available in nerd-fonts)
	 - goto release :
![img-1](https://github.com/masadsummair/oh-my-posh-window-guide/assets/62187782/10f889a0-5d1b-4464-95fa-511f1216edad)
	 - choose your favorite font and install its zip (choose from latest release):
![img-2](https://github.com/masadsummair/oh-my-posh-window-guide/assets/62187782/41498b6c-5f29-46b2-829d-eb9c3f0c4fcd)
		
 - then extract it and install it
 - install [oh my posh](https://ohmyposh.dev/docs/installation/windows)
## Installation
```
winget install JanDeDobbeleer.OhMyPosh -s winget
```
## Update
```
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```
For default theme enable:
```
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json" | Invoke-Expression
```

### Want more themes?
```
Get-PoshThemes
```

if you restart powershell everything will go away :)
no worries i got you.

### to check which shell are you in:

```
oh-my-posh get shell
```

if you are in powershell:

```
notepad $PROFILE
```

When the above command gives an error, make sure to create the profile first.

```
New-Item -Path $PROFILE -Type File -Force
```

In this scenario, it can also be that PowerShell blocks running local scripts. To solve that, set PowerShell to only require remote scripts to be signed using `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine`, or [sign the profile](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_signing?view=powershell-7.3#methods-of-signing-scripts).

Then add the following line in the file.(you can select any other theme )

```
oh-my-posh init pwsh --config 'C:\Users\${username}$\AppData\Local\Programs\oh-my-posh\themes\{themename}.omp.json' | Invoke-Expression>
```
