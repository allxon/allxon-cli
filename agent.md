Execute Allxon Agent utilities.

## `uninstall` 🔒

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

## `diagnose`

Check the network environment of your edge device.

**Example**

```bash
allxon-cli agent diagnose
```

## `proxy` 🔒

Set the proxy server for Allxon Agent.

**Example**

```bash
allxon-cli agent proxy --url "https://your-proxy-server.com"
```

## `pair`

Add device to Allxon Portal by pairing token.

**Options**

- `--pairing-token TEXT`: Input the pairing token to pair the device.
- `--name TEXT`: Set device name.
- `--profile TEXT`: Set device profile using a [Profile file](README.md#--profile-textfile).
- `--subscription-id TEXT`: Set *Subscription ID* to assign a seat for the device ([Learn more](https://www.allxon.com/knowledge/how-to-add-devices-and-assign-subscription-seats-using-allxon-cli)).

**Example**

```bash
allxon-cli agent pair --pairing-token "your-pairing-token"
allxon-cli agent pair --pairing-token "your-pairing-token" --name "device-name" --profile "profile.json" --subscription-id "your-subscription-id"
```