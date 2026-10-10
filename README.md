# xtool for linux

- install xtool for linux

## install swift

- please create a backup of the bashrc file

```sh
cp /home/user/.bashrc /home/user/.bashrc.backup
```

- the Swiftly installer manages Swift and its dependencies.

```sh
curl -O https://download.swift.org/swiftly/linux/swiftly-$(uname -m).tar.gz && \
tar zxf swiftly-$(uname -m).tar.gz && \
./swiftly init --quiet-shell-followup && \
. "${SWIFTLY_HOME_DIR:-$HOME/.local/share/swiftly}/env.sh" && \
hash -r
```

- output

```sh
.....................
Swiftly installs files into the following locations:

/home/user/.local/share/swiftly - Directory for configuration files
/home/user/.local/share/swiftly/bin - Links to the binaries of the active toolchain
/home/user/.local/share/swiftly/toolchains - Directory hosting installed toolchains

These locations can be changed by setting the environment variables
SWIFTLY_HOME_DIR, SWIFTLY_BIN_DIR, and SWIFTLY_TOOLCHAINS_DIR before running 'swiftly init' again.
.....................
```

- check version

```sh
swift --version
```

- install usbmuxd

```sh
sudo dnf install usbmuxd
```

## references

- check out [xtool installation linux](https://xtool.sh/documentation/xtool/installation-linux)
- check out [install swift linux](https://www.swift.org/install/linux/)
