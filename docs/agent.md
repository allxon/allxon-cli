Execute or update Allxon Agent Utilities.

## `install`
Install or update Allxon Agent.

**Example**
```bash
# default install
allxon-cli agent install
```

## `uninstall`
Uninstall Allxon Agent.

**Example**
```bash
allxon-cli agent uninstall
```

## `info`
Get the current Allxon Agent status.

**Example**
```bash
allxon-cli agent info
```

## `pairing-code`
Get the device pairing code for Allxon Portal.

**Example**
```bash
allxon-cli agent pairing-code
```

## `external-ca`
Configure the CA file of the transparent proxy server.

**Options**

`-f,--file TEXT:FILE`: Configure the path to the CA file.

`-r,--reset`: Reset the configuration of the CA settings.

`-s,--show`: Print ca content.

**Example**
```bash
allxon-cli agent external-ca --file your-ca.ca
```

## `proxy`
Configure the URL for the https proxy server.

**Options**

`-u,--url TEXT`: Configure the proxy server using a URL.

`-r,--reset`: Reset the configuration of the proxy server settings.

`-s,--show`: Print proxy url.

**Example**
```bash
allxon-cli agent proxy --url "https://your-proxy-server.com"
```

## `diagnose`
Check the network environment of your edge device.

**Example**
```bash
allxon-cli agent diagnose
```
                  
