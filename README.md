How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a command like this:

```bash
  repo init -u git://github.com/DevelLevel/android_manifest-AEX.git -b n-mr1
```

Clone n-mr1 vendor and configure

```bash
  git clone https://github.com/DevelLevel/android_vendor_sony_suzuran-AEX.git -b n-mr1 vendor/sony
  cd vendor/sony/
  cp -r qcom_copy/prebuilt/ ../qcom/
  rm -rf qcom_copy/
```
