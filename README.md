# Android SDK in SNAP-STORE

## Description 

  This is snap version of console sdk manager for Android. For more information about sdkmanager see official google [documentation](git@github.com:EndrII/sdkmanager-android.git) 
  
  ### sdkmanager 

  The sdkmanager is a command line tool that allows you to view, install, update, and uninstall packages for the Android SDK. If you're using Android Studio, then you do not need to use this tool and you can instead manage your SDK packages from the IDE. 
  The sdkmanager tool is provided in the Android SDK Tools package (25.2.3 and higher) and is located in android_sdk/tools/bin/. 
  
  #### Usage:
  
  All SKD files location in the snap home folder:
  
  ``` 
    ~/snap/android-sdk/current/AndroidSDK
  ```

  You can use the sdkmanager to perform the following tasks. 
  List installed and available packages 
  sdkmanager --list [options] 
  Install packages 
  sdkmanager packages [options] 
  The packages argument is an SDK-style path as shown with the --list command, wrapped in quotes (for example, "build-tools;29.0.0" or "platforms;android-28"). You can pass multiple package paths, separated with a space, but they must each be wrapped in their own set of quotes. 
  For example, here's how to install the latest platform tools (which includes adb and fastboot) and the SDK tools for API level 28: 
  sdkmanager "platform-tools" "platforms;android-28" 
  Alternatively, you can pass a text file that specifies all packages: 
  sdkmanager --package_file=package_file [options] 
  The package_file argument is the location of a text file in which each line is an SDK-style path of a package to install (without quotes). 
  To uninstall, simply add the --uninstall flag: 
  sdkmanager --uninstall packages [options] 
  sdkmanager --uninstall --package_file=package_file [options] 
  Update all installed packages 
  sdkmanager --update [options] 
  Options 
  The following table lists the available options for the above commands. 
  Option 	Description 
  --sdk_root=path 	Use the specified SDK path instead of the SDK containing this tool 
  --channel=channel_id 	Include packages in channels up to channel_id. Available channels are: 
  0 (Stable), 1 (Beta), 2 (Dev), and 3 (Canary). 
  --include_obsolete 	Include obsolete packages in the package listing or package updates. For use with --list and --update only. 
  --no_https 	Force all connections to use HTTP rather than HTTPS. 
  --verbose 	Verbose output mode. Errors, warnings and informational messages are printed.
  --proxy={http | socks} 	Connect via a proxy of the given type: either http for high level protocols such as HTTP or FTP, or socks for a SOCKS (V4 or V5) proxy. 
  --proxy_host={IP_address | DNS_address} 	IP or DNS address of the proxy to use. 
  --proxy_port=port_number 	Proxy port number to connect to.  


## Install

    sudo snap install android-sdk
    snap connect android-sdk:android-config

## Build
    sudo snap install snapcraft --classic
    snapcraft 
