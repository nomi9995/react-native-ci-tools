# Horizon continuous integration tools

Change application bundle name and ID on the fly (build time) for both Android and IOS

Usage: rename-horizon [options] [command]


  Commands:

    bundle <bundleId> <bundleName>  Change application bundle ID and name (display name)

  Options:

    -h, --help                             output usage information
    -i, --ios                              Appy changes to IOS project (IOS .plist files)
    -a, --android                          Appy changes to Android project (Android Manifest and Java classes)
    --directory <projectDirectory>         project main directory (absolute)
    --iosSubDir <iosSubDirectory>          IOS project sub directory (relative)
    --androidSubDir <androidSubDirectory>  Android project sub directory (relative)


  Example:

    * feed in project location [Ios and Android]
    rename-horizon bundle "MyApp.UAT" "APP UAT" -ia --directory /Users/myUser/src/Cool/Project

    * without project location (automatically use current location) [Ios and Android]
    rename-horizon bundle "BigApp.Build.300" "BIG App 300" -ia 

    * with project location but chnage android only [Android (-a flag)]
    rename-horizon bundle "NANdroid.X" "NANdroid X" -a


  
  Coming soon:

    - Resize icons (gd resize and slice)
    - Lable icons on build (add text overlay on app icon)
    - Generate app info json to be used in presenation layer (git sha, build type, build number)