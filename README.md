How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a command like this:

```bash
  repo init -u git://github.com/DevelLevel/android.git -b n-mr1
```

sync

```bash
  repo sync -c -jx --force-sync --no-clone-bundle --no-tags
```

Clone n-mr1 vendor and configure

```bash
  git clone https://github.com/DevelLevel/android_vendor_sony.git -b n-mr1 vendor/sony
  cd vendor/sony/
  cp -r qcom_copy/prebuilt/ ../qcom/
  rm -rf qcom_copy/
```

Revert commits from the thermalmanager, they are causing build issues...

```bash
cd vendor/oss/thermanager
git revert 7010b705245e804bac0dcea4d8783125ef47caac
git revert 4112bb631c57b5b42e5c20b7a26c59e34692100b
```

Then build!


```bash
. build/envsetup.sh
lunch aosp_device_codename-userdebug
make aex -jx
```
