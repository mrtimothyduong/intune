# Intune Notes
A list of Intune notes

## Dynamic Device Groups

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
