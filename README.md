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
