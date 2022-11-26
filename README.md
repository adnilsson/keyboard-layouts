# Keyboard layouts for Windows

Created with Keyboard Layout Creator 1.4.6000.2


## Bulid issues

### *Name* already exists

If you find an error with your layout that you wish to change, you need to:
1. Uninstall the layout
  * Through Add/Remove Programs or through the original installer (if still available)
2. Make the change and re-build the layout
3. Install the updated layout
4. Reboot (maybe just sign out and log back in)

If, in step 2., the build fails with an error similar to "*name-of-layout* already exists",  it proabably means that the layout was not completely removed from your system when it was uninstalled.
The MS-forums provided [some help](https://social.msdn.microsoft.com/Forums/en-US/6e143a03-3fda-43fd-831b-2c3056d732b1/how-do-i-remove-a-keyboard-layout?forum=windowsuidevelopment) with this, for once.
Open the registry editor and look for something similar to:
```
HKEY_LOCAL_MACHINE\SYSTEM\ControlSet002\Control\Keyboard Layouts
```

Your layout file is likely among the last ones under `Keyboard Layouts`.
Remove it once you find it, reboot, and try again.
