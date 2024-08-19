# Allxon CLI manual

Allxon CLI or `allxon-cli`, is a command-line interface to Allxon for use in your terminal or your scripts.

[![asciicast](https://asciinema.org/a/m4pz3rf9sO9Jfc2zcrvVl3PhE.svg)](https://asciinema.org/a/m4pz3rf9sO9Jfc2zcrvVl3PhE)

## Installation

The `allxon-cli` is installed automatically when you install the Allxon Agent, follow [link](https://www.allxon.com/knowledge/install-allxon-agent-via-command-prompt) instruction to install agent.
After that, your can following command to show current `allxon-cli` version.

```
allxon-cli version
```

> On Windows, you may need to add the installed path (`C:\Program Files\allxon-cli\bin`) to the PATH environment variable in order to run the `allxon-cli` from anywhere. Or you can install from [release page](https://github.com/allxon/allxon-cli/releases) manually.

## Reference

- [`allxon-cli agent`](agent.md)
- [`allxon-cli plugin`](plugin.md)
- [`allxon-cli ota`](ota.md)
- [`allxon-cli log`](log.md)
- [`allxon-cli version`](version.md)

> The symbol '🔒' means the command is require root permission / administrator authorization.

# Linux online installer

Online installer provide a simple way to install Allxon Agent on Linux system. The script will install the latest version of Allxon Agent and `allxon-cli` automatically.

Following commands to install Allxon Agent on Linux system:

```bash
sudo bash -c "$(wget -qO - https://get.allxon.net/linux)" -s [options] [arguments]

# Default install
sudo bash -c "$(wget -qO - https://get.allxon.net/linux)"
```

## Options

- `--release TEXT`: Install a specific version of Allxon Agent; default is the latest version. 
- `--release-file TEXT:FILE`: Install Allxon Agent from a local file.
- `--no-ui`: Disable Allxon Agent UI installation.
- `--silent`: Skip all prompts.
- `--skip-launch`: Skip launching Allxon Agent after installation.
- `--uninstall`: Uninstall Allxon Agent.
- `--help`: Show help message and exit.
- `--version`: Show version and exit.

## Options with enrollment settings
Device will be automatically enrolled with the specified settings.
> ❗Options only work with first time installation.

- `--token TEXT`: Add device using [*Add-Device Booster*](https://www.allxon.com/knowledge/how-to-set-up-add-device-booster) token. 
- `--subscription-id TEXT`: Set *Subscription ID* to assign a seat for the device ([Learn more](https://www.allxon.com/knowledge/how-to-add-devices-and-assign-subscription-seats-using-allxon-cli)). 
  > ❗️Must be used with `--token` option.
- `--name TEXT`: Set device name.
- `--profile TEXT:FILE`: Set device profile using a [Profile file](#profile-textfile).
- `--region TEXT`: Set the server region(`'US'`, `'JP'`) for Allxon Agent .
- `--proxy TEXT`: Set proxy url for Allxon Agent installation and environment.

### Details

#### `--profile TEXT:FILE`: 

Profile file is a json file that contains the fields under Profile section in the Allxon Protal. The file can be used to set the profile during installation. The file should be in the following format:

```json
{
    "store": "My Store",
    "phone": "12345678",
    "asset": "ASSET123",
    "address": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "country": "USA",
    "zip": "12345",
    "note": "This is a note",
    "tags": [
        "tag1"
    ]
}
```

> Country should be in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements) format.


# Windows wizard installer

Powershell version of online installer provide a simple way to install Allxon Agent on Windows system. The script will install the latest version of Allxon Agent and `allxon-cli` automatically.

```powershell
Invoke-WebRequest -Uri "https://dev.allxon.net/windows/allxon-installer.ps1" -OutFile "$env:TEMP\allxon-installer.ps1"; & "$env:TEMP\allxon-installer.ps1"
```
