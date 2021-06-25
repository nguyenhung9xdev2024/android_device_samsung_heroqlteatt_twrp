# TWRP for Galaxy Tab S3 (gts3llte)

## How to build

Set up AOSP build environment before following this guide.

Create a project directory and prepare to pull the source tree.

```bash
mkdir twrp-9.0; cd twrp-9.0
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
```

Create a manifest file to clone this repository.

```bash
mkdir .repo/local_manifests
vi .repo/local_manifests/gts3llte.xml
```

Put this content into that file.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
    <project name="awesometic/android_device_samsung_gts3llte-twrp"
        path="device/samsung/gts3llte"
        revision="android-9.0"
        remote="github" />
</manifest>
```

Sync and build.

```bash
repo sync
. build/envsetup.sh ; lunch omni_gts3llte-eng ; mka recoveryimage
```

## Credits

- [Android Open Source Project](https://source.android.com/)
- [TeamWin](https://twrp.me/)
- [LineageOS](https://lineageos.org/)
- [OmniROM](https://omnirom.org/)
- [TWRP Minimal Manifests](https://github.com/minimal-manifest-twrp)

## Special Thanks to

- Valera1978 for his previous work including his MSM8996 kernel
- ashyx for his previous work on TWRP

## License

```xxx
Copyright 2021 Deokgyu Yang <secugyu@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
