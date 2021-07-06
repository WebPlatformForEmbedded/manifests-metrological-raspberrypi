# manifests-metrological-raspberrypi
Git-repo manifests for building the RaspberryPi with Yocto

## Setting up the build
1. Initialize a repo workspace with one of the manifests present in this repository. I.e to create
a build based on Yocto Dunfell execute:
```shell
repo init -u git@github.com:WebPlatformForEmbedded/manifests-metrological-raspberrypi.git -m dunfell-main.xml -b main
```
2. Synchronize meta layers with the corresponding remote repositories.
```shell
repo sync
```
3. Source the build environment setup script. I.e for Dunfell builds 
```shell
source setup-rpi.sh
```

4. Trigger a build for the rpi target.
```shell
bitbake wpe-eglfs-image
```
---
