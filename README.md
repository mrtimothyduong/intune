# Intune Notes
A list of Intune notes

## Dynamic deviceOSType Syntaxes
DeviceOSType | Eq / Contains | Syntax
--- | --- | ---
iPhones | eq | iPhone
iPads | eq | iPad
All Android | contains | Android
Android Enterprise | Eq | AndroidEnterprise
Android For Work | Eq | AndroidForWork
All Windows | contains | Windows
All Mac Devices | contains | Mac
Mac DEP | eq | MacMDM


## Example Dynamic Device Groups

All Devices under Intune Management
```
(device.managementType -eq "MDM")
```

All Corporate Devices
```
(device.deviceOwnership -eq "Company")`
```

iPads & iPhones
```
(device.deviceOSType -eq "iPad") -or (device.deviceOSType -eq "iPhone")
```

Android Devices
```
(device.deviceOSType -contains "Android")
```

Android Enterprise
```
(device.deviceOSType -contains "AndroidEnterprise")
```

MacOS Devices
```
(device.deviceOSType -contains "Mac")
```

MacOS DEP Devices
```
(device.deviceOSType -contains "MacMDM")
```
