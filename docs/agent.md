Execute or update Allxon Agent Utilities.

## `uninstall`

Uninstall Allxon Agent.

*Require administrator or root permission*

**Example**

```bash
allxon-cli agent uninstall
```

## `info`

Get the current Allxon Agent status.

*Require administrator or root permission*

**Example**

```bash
allxon-cli agent info
```

## `pairing-code`

Get the device pairing code for Allxon Portal.

**Options**

`--proxy TEXT`: Configure the URL for the https proxy server.

`--external-ca TEXT:FILE`: Configure the CA file of the transparent proxy server.

**Example**

```bash
allxon-cli agent pairing-code
```

## `external-ca`

Configure the CA file of the transparent proxy server.

*Require administrator or root permission*

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

*Require administrator or root permission*

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

*Require administrator or root permission*

**Options**

`--proxy TEXT`: Configure the URL for the https proxy server. (Linux only)

`--external-ca TEXT:FILE`: Configure the CA file of the transparent proxy server. (Linux only)

**Example**

```bash
allxon-cli agent diagnose
```
