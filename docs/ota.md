Allxon OTA artifact toolkit

## `make`

Make a Allxon ota artifact package from given directory which contain `ota_deploy.sh`.

**Options**

- `-d, --directory TEXT:DIRECTORY`: The folder to generate an OTA artifact (required).

**Example**

Provide a path with `ota_deploy.sh` inside.

```
allxon-cli ota make --directory /path/to/ota_content
```

## `test`

Test a Allxon ota artifact deployment on local device.

*Require administrator or root permission*

**Options**

- `-f, --file TEXT:FILE`: test FILE ota package on local device (required).

**Example**

```
allxon-cli ota test --file 505b22463d94220de326ec610b66e7e7-Allxon_OTA_Artifact-L-x86_64.tar.gz
```
