Show cache of the Configs and Alerts for Allxon Agent and Plugins.

## Options

- `--app-guid TEXT`: Input the Plugin's App GUID to show cache of the Configs and Alerts.

## `config`

Show cache of the Configs for Allxon Agent and Plugins.

**Options**

- `--format`: Output in formated JSON.

**Example**

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd config 
```

## `alarm`

Show cache of the Alerts for Allxon Agent and Plugins.

**Options**

- `--format`: Output in formated JSON.

**Example**

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd alarm 
```

## `install` 🔒

Install plugin.

**Options**

- `-p, --package TEXT:FILE`: Input the Plugin's package path to install.

**Example**

Install plugin by App GUID from Allxon plugin center.

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd install
```

Install plugin by package path.

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd install --package /path/to/plugin/package
```

## `upgrade` 🔒

Upgrade plugin.

**Example**

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd upgrade
```

## `uninstall` 🔒

Uninstall plugin.

**Example**

```bash
allxon-cli plugin --app-guid 8102220f-080f-4f12-a413-6ccb2c786fgd uninstall
```
