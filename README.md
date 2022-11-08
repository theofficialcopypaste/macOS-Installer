# MacOS USB Installer
How to create macOS USB Installer?

## Download Tools

### Terminal Based

* [gibMacOS](https://github.com/corpnewt/gibMacOS)

  **Support**: Linux, Mac, Windows 

	Example:
	```zsh
	  #######################################################
	 #                Downloading Catalog                  #
	#######################################################
	
	Currently downloading publicrelease catalog from:
	
	https://swscan.apple.com/content/catalogs/others/index-12-10.16-10.15-10.14-10.13-10.12-10.11-10.10-10.9-mountainlion-lion-snowleopard-leopard.merged-1.sucatalog
	
	Downloaded 6.92 MB of 6.92 MB (100.00%)
	```
	```zsh
	  #######################################################
	 #                    Parsing Data                     #
	#######################################################
	
	Scanning products after catalog download...
	
	 -->  1. macOS Mojave (18F2059)
	 -->  2. macOS Mojave (18G103)
	 -->  3. macOS High Sierra (17G66)
	 -->  4. macOS Mojave (18E2034)
	 -->  5. Install macOS High Sierra Beta (17F66a)
	 -->  6. macOS Catalina (19D2064)
	```
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

### GUI Based

* [Mist](https://github.com/ninxsoft/Mist)

  **Support**: Mac, with multiple option `.app`, `.dmg`, `.iso` and `.pkg`

<div align=center>

![2022-11-07_13-57-22](https://user-images.githubusercontent.com/72515939/200236489-583e706f-4390-4867-ad12-4b7a3af41bb3.png)
![2022-11-07_14-07-53 (1)](https://user-images.githubusercontent.com/72515939/200238406-34b183c2-6350-4af3-a509-3aa1b9b6fb47.png)

</div>

< **Note**: Refer [Mr. Macintosh](https://mrmacintosh.com/how-to-download-macos-catalina-mojave-or-high-sierra-full-installers/) for various alternative download methods.

## Create USB

1. Hit `Cmd + Space` and type Disk Utility

<div align=center>
	
![2022-11-08_19-44-07](https://user-images.githubusercontent.com/72515939/200556302-a123350b-b392-4b5e-8a55-84251240dd2c.png)
	
</div>	

2. Click View and Show All Devices

<div align=center>
	
![2022-11-08_19-48-20](https://user-images.githubusercontent.com/72515939/200556508-966a6215-2d54-4bde-a095-c2c9d457eb4b.png)
	
</div>

3. Choose any disk / USB Drive (Recommend 18GB+), Erase, Rename disk as `MyVolume` as Mac OS Extended (Journal) using GUID Partition Map.

<div align=center>
	
![2022-11-08_19-44-45](https://user-images.githubusercontent.com/72515939/200556573-1ca0e3f7-823d-4405-abb4-91de62ae61a3.png)
![2022-11-08_19-46-21 (1)](https://user-images.githubusercontent.com/72515939/200556663-d18f5f7d-38d6-4f3b-a27c-fcb02912f2d7.png)
![2022-11-08_19-45-45](https://user-images.githubusercontent.com/72515939/200556672-a05c61c7-f4ec-4fc4-b41f-1e4745faeca6.png)
	
</div>

4. Extract Install macOS XXXX.app from Install macOS xxxx.dmg (Manual) to /Applications or install downloaded InstallAssistant.pkg using [gibMacOS](https://github.com/corpnewt/gibMacOS) (Automatically move .apps to /Applications), open Terminal, paste macOS Install code and hit `Return` / `Enter`. Please follow further Instruction.

## Install Code 

> **Note**: This code only work on macOS. (Require to move Install macOS XXXXXX.app to /Application)

### Ventura
```zsh
sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### Monterey
```zsh
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### Big Sur
```zsh
sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### Catalina
```zsh
sudo /Applications/Install\ macOS\ Catalina.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### Mojave
```zsh
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### High Sierra
```zsh
sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

### El Capitan
```zsh
sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app
```
