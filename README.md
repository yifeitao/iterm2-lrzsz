# iterm2-lrzsz

Config iterm2 to use lrzsz on macOS

## Install

### 1. Install lrzsz

```shell
brew install lrzsz
```

### 2. Download `zmoden-rz` and `zmoden-sz` into `/usr/local/bin`

```shell
sudo chmod 777 /usr/local/bin/zmodem-*
```

### 3. Config iterm2

profiles -> default -> editProfiles -> Advanced, and choose Tirggers

Add two Trigger:

```shell
# sz
Regular expression: \*\*B0100
Action: Run Silent Coprocess
Parameters: /usr/local/bin/zmodem-sz.sh
Instant: checked
# rz
Regular expression: \*\*B00000000000000
Action: Run Silent Coprocess
Parameters: /usr/local/bin/zmodem-rz.sh
Instant: checked
```
