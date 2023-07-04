###### MORBIOS ######

### Initialize local repository ###
```bash
mkdir Morb
```
```bash
cd Morb
```
### Sync ###

```bash
repo init -u https://github.com/Morbi-OS/manifest.git -b 13
```

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

source build/envsetup.sh
```
```bash
lunch aosp_$device-userdebug
```
```bash
mka bacon -j64
```
