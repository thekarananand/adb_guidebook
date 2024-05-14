# Android Debugging Bridge Guidebook

### List Apps

```
adb shell pm list packages
```

### Get APK files

1. Get Path to APK

    ```
    adb shell pm path <PACKAGE_NAME>
    ```

2. Copy it

    ```
    adb pull <APK PATH> <DESTINATION>
    ```

### Install Preinstalled App

```
adb shell pm install-existing <PACKAGE_NAME>
```

### Bypass "[DELETE_FAILED_USER_RESTRICTED]" on vivo/iqoo

1. Android 13
    ```
    adb shell service call package 131 s16 <PACKAGE_NAME> i32 0 i32 0
    ```

2. Android 12
    ```
    adb shell service call package 134 s16 <PACKAGE_NAME> i32 0 i32 0
    ```
