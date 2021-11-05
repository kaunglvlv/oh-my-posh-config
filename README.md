Oh My Posh (Configuration)
===

My [Oh My Posh](https://ohmyposh.dev) configuration I use on terminals.

Installation
---

To start, clone the repo

```
git clone https://github.com/kkaung/oh-my-posh-config
```

Windows
---

### Install Terminal

```
winget install Microsoft.WindowsPowershell
```

### Install Powershell (Core)

```
winget install Microsoft.Powershell
```

### Set Powershell as the default on Terminal

* Open **Terminal**
* Click dropdown chevron
* Select **Settings**
* Select **Powershell** (_not_ Windows Powershell) as **Default Profile**
* Restart Terminal or open new tab

### Install Oh My Posh

Open terminal and run

```
winget install JanDeDobbeleer.OhMyPosh
```

### Install Nerd Fonts

Oh My Posh uses special glyphs that come with certain fonts.

Download and install [Caskaydia Cove Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip).

### Create/Edit Powershell Profile

To automatically run Oh My Posh with every command, we need to create/edit the profile script. To find out where it lives, type the following in Terminal

```
$PROFILE
```

This will give you a path like `C:\users\me\Documents\PowerShell\Microsoft.PowerShell_profile.ps1`. If this file does not exist, create it in this path.

Then edit the file with the following content and _replace_ `C:\my\cloned\path\` with the directory of the cloned repo path.

```
oh-my-posh --init --shell pwsh --config C:\my\cloned\path\oh-my-posh-config\config.json | Invoke-Expression
```

### Update Font

Go to your Terminal Settings:

* Click on **Powershell** under _Profiles_
* Go to the **Appearance** tab and select **CaskaydiaCove NF** font face
  * You can also make this the default font by going to **Defaults** under _Profiles_ and setting the font face under the **Appearance** tab

#### VS Code

* Go to **Settings**
* Search for font
* Under **Font Family** add (in quotes) `'CaskaydiaCove NF'`

Example

```
'CaskaydiaCoveNF', Consolas, 'Courier New', monospace
```

Mac
---

### Install zsh

```
brew install zsh
```

To ensure we're using the zsh that we've installed, open **Terminal** and run

```
which zsh
```

Take the path and update **Terminal Preferences** > **Shell opens with Command**.

### Install Oh My Posh

```
brew tap jandedobbeleer/oh-my-posh
brew install oh-my-posh
```

### Create/Edit .zshrc

To automatically run Oh My Posh with every command, we need to update zsh config. Create/edit `~/.zshrc` with the following content and _replace_ `~/my/cloned/repo` with the directory of the cloned repo path.

```
eval "$(oh-my-posh --init --shell zsh --config '~/my/cloned/repo/oh-my-posh-config/config.json')"
```

### Install Nerd Fonts

Oh My Posh uses special glyphs that come with certain fonts.

Download and install [Meslo Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Meslo.zip).

_Note: You will only need to install `Meslo LG M Regular Nerd Font Complete.tff` but can install different font weights and sizes if you prefer._

### VS Code

* Go to **Settings**
* Search for font
* Under **Font Family** add (in quotes) `'MesloLGM Nerd Font'`

Example

```
'MesloLGM Nerd Font', Menlo, Monaco, 'Courier New', monospace
```
