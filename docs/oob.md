Execute oob related Utilities.

## `scan`
Scan com port.

**Example**
```bash
allxon-cli oob scan
```

## `heartbeat`
Heartbeat function.

**Options**

- `-p,--port`: Target com port (required)

### `ping`
Send heartbeat signal.

### `disable`
Disable heartbeat.

**Example**
```bash
allxon-cli heartbeat --port ttyUSB0 ping
```

## `link`
Link to oob.

- `-m,--manual TEXT`: Link oob manually.

**Example**
```bash
allxon-cli oob link
```
