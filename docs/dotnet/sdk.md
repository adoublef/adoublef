# dotNET: SDK

This documentation will be an overview of how to setup a Linux system to start developing **dotNET** applications.

---

## Installing the SDK

This will assume the host device is running a Debian 11, for other platforms visit [here](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)

In the terminal we can use the following command:

```bash
wget https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

This will add the Microsoft package signing key to the list of trusted keys.

To install the SDK the following command is needed:

```bash
sudo apt-get update && \
sudo apt-get install -y dotnet-sdk-7.0
```

Finally we can install the runtime using the command:

```bash
sudo apt-get install -y dotnet-runtime-7.0
```

### Updating dotNET

To update when a new patch is released we can use the following command:

```bash
sudo apt-get update
sudo apt-get upgrade
```

To verify installation use the following command:

```bash
dotnet --version
```