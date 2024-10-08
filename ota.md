Allxon OTA artifact toolkit

## `make`

Make a Allxon ota artifact package from given directory which contain `ota_deploy.sh`.

**Options**

- `-d, --directory TEXT:DIRECTORY`: The folder to generate an OTA artifact (required).
- `-a, --architect TEXT`: The architecture of the OTA artifact [x86_64|aarch64|all] (default: host architecture).

**Example**

Provide a path with `ota_deploy.sh` inside.

```
allxon-cli ota make --directory /path/to/ota_content
allxon-cli ota make --directory /path/to/ota_content --architect x86_64
```

## `test` 🔒

Test a Allxon ota artifact deployment on local device.

**Options**

- `-f, --file TEXT:FILE`: test FILE ota package on local device (required).
- `--args [TEXT, TEXT]...`: Additional arguments to pass to the `ota_deploy.sh`.
> Note: The arguments should be in key-value pairs.

**Example**

Linux bash:
```bash
allxon-cli ota test --file 505b22463d94220de326ec610b66e7e7-Allxon_OTA_Artifact-L-x86_64.tar.gz

# Pass additional arguments to the ota_deploy.sh
allxon-cli ota test --file 505b22463d94220de326ec610b66e7e7-Allxon_OTA_Artifact-L-x86_64.tar.gz --args "name1" "value1" "name2" "value2"

# Pass additional arguments like this to the ota_deploy.sh after executing the command
# ota_deploy.sh --name1='value1' --name2='value2'
```

Windows batch:
```batch
allxon-cli.exe ota test --file 505b22463d94220de326ec610b66e7e7-Allxon_OTA_Artifact-W-x86_64.zip --args "name1" "value1" "name2" "value2"

:: Pass additional arguments like this to the ota_deploy.bat after executing the command
:: ota_deploy.bat --name1='value1' --name2='value2'
```

