# MacOS USB Installer
How to create macOS USB Installer?

## Download Tools

### Terminal Based

[**gibMacOS**](https://github.com/corpnewt/gibMacOS) (Linux, Mac, Windows)

```zsh
  #######################################################
 #                      gibMacOS                       #
#######################################################
	
Available Products:
	
1. macOS Big Sur 11.7.1 (20G918)
   - 012-90253 - Added 2022-10-24 17:16:38 - 12.42 GB
2. macOS Monterey 12.6.1 (21G217)
   - 012-90254 - Added 2022-10-24 17:15:48 - 12.41 GB
3. macOS Ventura 13.0 (22A380)
   - 012-92138 - Added 2022-10-24 17:14:11 - 12.16 GB
4. macOS Big Sur 11.7 (20G817)
   - 012-38280 - Added 2022-09-20 17:15:39 - 12.42 GB
5. macOS Monterey 12.6 (21G115)
   - 012-40494 - Added 2022-09-20 17:14:37 - 12.40 GB
6. macOS Monterey 12.5.1 (21G83)
   - 012-51693 - Added 2022-08-24 17:13:27 - 12.41 GB
	
M. Change Max-OS Version (Currently 12)
C. Change Catalog (Currently publicrelease)
I. Only Print URLs (Currently Off)
S. Set Current Catalog to SoftwareUpdate Catalog
L. Clear SoftwareUpdate Catalog
R. Toggle Recovery-Only (Currently Off)
U. Show Catalog URL
Q. Quit
	
Please select an option:  
```

> **Note**: This tool will download multiple packages. BigSur+ and certain Catalina versions require `InstallAssistant.pkg` to build the apps. Mojave and below, require `BuildmacOSInstallApp.command` from [gibMacOS](https://github.com/corpnewt/gibMacOS).

[**Mist-Cli**](https://github.com/ninxsoft/mist-cli) (Mac)

<div align=center>

![Cli](https://github.com/ninxsoft/mist-cli/raw/main/README%20Resources/Firmwares.png)
![Cli2](https://github.com/ninxsoft/mist-cli/raw/main/README%20Resources/Installers.png)

</div>
	
> **Note**: A Mac command-line tool that automatically downloads macOS `Firmwares` / `Installers`. Alternatively, install via [Homebrew](https://brew.sh) by running `brew install mist`

### GUI Based

[Mist](https://github.com/ninxsoft/Mist) (Mac, with multiple option `.app`, `.dmg`, `.iso` and `.pkg`)

<div align=center>

![2022-11-07_13-57-22](https://user-images.githubusercontent.com/72515939/200236489-583e706f-4390-4867-ad12-4b7a3af41bb3.png)
![2022-11-07_14-07-53 (1)](https://user-images.githubusercontent.com/72515939/200238406-34b183c2-6350-4af3-a509-3aa1b9b6fb47.png)

</div>

> **Note**: A Mac utility that automatically downloads macOS `Firmwares` / `Installers`.

## Create USB

1. Hit `Cmd + Space` and type Disk Utility
2. Click View and Show All Devices
3. Choose any disk / USB Drive (Recommend 18GB+), Erase, Rename disk as `MyVolume` as Mac OS Extended (Journal) using GUID Partition Map.
4. Extract Install macOS xxxx.app from Install macOS xxxx.dmg (Manually) to /Applications or install downloaded InstallAssistant.pkg using [gibMacOS](https://github.com/corpnewt/gibMacOS) (Automatically move .apps to /Applications), open Terminal, paste macOS Install code and hit `Return` / `Enter`. Please follow further Instruction.

> **Note**: Refer [Mr. Macintosh](https://mrmacintosh.com/how-to-download-macos-catalina-mojave-or-high-sierra-full-installers/) for various alternative download methods.

## Install Code 

* **Ventura**
```zsh
sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **Monterey**
```zsh
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **Big Sur**
```zsh
sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **Catalina**
```zsh
sudo /Applications/Install\ macOS\ Catalina.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **Mojave**
```zsh
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **High Sierra**
```zsh
sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

* **El Capitan**
```zsh
sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app
```

> **Note**: This code only work on macOS. (Require to move Install macOS xxxx.app to /Application)
