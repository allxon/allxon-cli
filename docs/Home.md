# Allxon CLI manual
Allxon CLI or `allxon-cli`, is a command-line interface to Allxon for use in your terminal or your scripts.

[![asciicast](https://asciinema.org/a/m4pz3rf9sO9Jfc2zcrvVl3PhE.svg)](https://asciinema.org/a/m4pz3rf9sO9Jfc2zcrvVl3PhE)

## Installation
The `allxon-cli` is installed automatically when you install the Allxon Agent, follow [link](https://www.allxon.com/knowledge/install-allxon-agent-via-command-prompt) instruction to install agent.
After that, your can following command to show current `allxon-cli` version.

```
allxon-cli version
```

ℹ️ On Windows, you may need to add the installed path (`C:\Program Files\allxon-cli\bin`) to the PATH environment variable in order to run the `allxon-cli` from anywhere.

Or you can install from [release page](https://github.com/allxon/allxon-cli/releases) manually.

## Reference
- [`allxon-cli agent`](agent.md)
- [`allxon-cli oob`](oob.md)
- [`allxon-cli log`](log.md)
- [`allxon-cli version`](version.md)

# Linux online installer
Online installer provide a simple way to install Allxon Agent on Linux system. The script will install the latest version of Allxon Agent and `allxon-cli` automatically.

Following commands to install Allxon Agent on Linux system:
```bash
sudo bash -c "$(wget -qO - https://get.allxon.net/linux)" -s [options] [arguments]

# Default install
sudo bash -c "$(wget -qO - https://get.allxon.net/linux)"
```

## Options 
- `--release TEXT`: Install specific version of Allxon Agent, default is latest version.
- `--release-file TEXT`: Install Allxon Agent from local file.
- `--group-token TEXT`: Set group token for Allxon Agent enrollment.
- `--proxy TEXT`: Set proxy url for Allxon Agent installation and environment. 
- `--external-ca TEXT`: Set external CA certificate path (transparent proxy) for Allxon Agent installation and environment.
- `--no-ui`: Disable Allxon Agent UI installation.
- `--silent`: Skip all prompts.
- `--skip-launch`: Skip launch Allxon Agent after installation.
- `--uninstall`: Uninstall Allxon Agent.
- `--help`: Show help message and exit.
- `--version`: Show version and exit.

# Windows wizard installer
Windows wizard installer provide a gui wizard style to install Allxon Agent on Windows system. The wizard will install specfic version of Allxon Agent and `allxon-cli` depend on wizard version.

Download wizard installer from [release page](https://github.com/allxon/allxon-cli/releases).

Following command to execute wizard through command line mode:
```cmd
allxon-installer.exe --confirm-command install [options]=[arguments]

@REM Install with group token
allxon-installer.exe --confirm-command install group-token=dTvCX2QuT9C-cQnFYhoqda6588088583
```