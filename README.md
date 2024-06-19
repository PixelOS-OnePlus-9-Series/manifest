# manifest

```
mkdir PixelOS && cd PixelOS

repo init -u https://github.com/PixelOS-AOSP/manifest.git -b fourteen --git-lfs

mkdir .repo/local_manifests && wget https://raw.githubusercontent.com/PixelOS-OnePlus-9-Series/manifest/main/lemonadep.xml -O .repo/local_manifests/lemonadep.xml

repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)

lunch aosp_lemonadep-ap1a-user

mka bacon  -j$(nproc --all)
```