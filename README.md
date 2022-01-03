Manifest of LightX-Project ROM (Small AOSP Fork)
===========


Start off by following these steps:
----------------------


Create the directories
----------------------

As a first step, you'll have to create and enter a folder with the appropriate name.
To do that, run these commands:

```bash
   mkdir light
   cd light
```

To initialize your local repository, run this command:
------------------------------------------------------

```bash
   repo init -u https://github.com/LightX-Project/manifest -b lx-12.0
```

Afterwards, sync the source by running this command:
----------------

```bash
repo sync --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```


Building LightX
---------------

In case you are building Mac OS X, you are required to install coreutils from MacPorts before you continue.
In order to build, use this command:
```bash
   . build/env*
   lunch lightx_<devicecodename>-userdebug
   mka bacon -j$(nproc --all)
```
