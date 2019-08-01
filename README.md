# Boot setup utils

This project enables you to configure device properties such as **hostname** using a file on `/boot` partition like you enable *ssh* or *wi-fi* on Raspberry Pi.

## Usage

- Create `bootsetup` folder in `/boot` partition (only partition seen in Windows), here will reside all config files (Note: Some files may disappear during configuration process).
- Configure different parameters, see [docs folder](docs).

## Installing

``` bash
# Build .deb file
make

# Copy .deb from dist/ to target device

# Install .deb
dpkg -i <name>.deb
```

## Config folder structure

```
/boot/bootsetup
	hostname # Sets device hostname
	sshauth-USER # Add SSH keys to authorized_keys for user
	sshreset # Reset SSH keys
	upgrade # Update & upgrade using apt
```
