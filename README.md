# Raspberry Pi with Ubuntu server

Download and install image with balena etcher or similar

```
xz --decompress ubuntu-20.04.1-preinstalled-server-arm64+raspi.img.xz
sudo dd bs=4M if=ubuntu-20.04.1-preinstalled-server-arm64+raspi.img of=/dev/<REPLACE> status=progress
```

[Ubuntu for Raspberry Pi 4 image](https://ubuntu.com/download/raspberry-pi/thank-you?version=20.04&architecture=arm64+raspi)

### Wifi (Optional)
inside system-boot partition modify network-config ucomment and modify:
```yaml
wifis:
  wlan0:
  dhcp4: true
  optional: true
  access-points:
    "<wifi network name>":
      password: "<wifi password>"
```
