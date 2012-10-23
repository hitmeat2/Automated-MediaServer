Install CentOS 6 -------------------------------------------
	
	*This will erase all previous data from the machine you are loading it onto, proceed with caution.
			
			1) Make sure the machine is powered off.
			2) Insert the OS Loader USB Drive.
					*Before you start
						a) Ensure the Internet is connected via cat5 cable (Cord /No Wireless)
						b) Ensure at Boot-up you have the boot from USB option available.
						c) *If you do not have the boot from USB option, you will need to install via CD-ROM
						d) **If you cannot install via CD-ROM you will need a technician to pre-install to your hard-drive
			3) Select Your Language (English)
			4) Select Your Country (US)
			5) Select (URL) for Installation Method
			6) Configure TCP/IP
					*Ensure the asterick is selected in both categories, and that the first option is selected. (Just Like Below)
								
								[*] Enable IPv4 support
											(*) Dynamic IP Config
											( ) Manual config
								
								[*] Enable IPv6 support
											(*) Automatic
											( ) Dynamic
											( ) Manual
											
			7) After Network Manager has setup your connection, Type in the following URL
					
					"http://mediaserver.ronnieblue.com/centos6" after typing the URL
					*Do not Enable anything, or type any passwords. Just click OK.
					**This will download the current version of CentOS6 and prepare it for install onto your system.
					***It could Take a long time depending on the speed of your network connection.
			8) After the Initial Installation is done, Select "Use Text Mode"
			9) Use system clock is pre-selected, Select America/New York
			10) Type the password "mediaserver" twice. Make sure its lower case.
			11)Select Use Entire Hard Drive
			12) Make sure the first drive is not selected only sdb. Select OK
			12) Select write Changes to Disk.
			14) After the Files have downloaded and are installed, Remove the thumb drive.
			15) Select Reboot.
			16) At the grub prompt Type: grub>"root (hd0,0)" and press ENTER.
			17) Then Type: "setup (hd0)".
			18) After the setup has ran Type: "reboot".		
			19) The system will reboot immediately.
					*A 3 second timer will start. you need to press any key before the time runs out to go into boot-up config mode.
					 **If the time runs out, the machine will continuously restart. You will have to start over from step (19).
					 a) With CentOS highlighted PRESS "e" to edit the boot process.
					 b) You will now be temporarily changing the root from (hd1,0) to (hd0,0). Press "e" again with root highlighted.
					 c) Backspace all the writing currently on the line then Press "Tab". An error show up, Don't worry it's normal.
					 d) Type: "root (hd0,0)" on the line. (Ensure you type it exactly as written inside the " " or you will get an errer message. Press ENTER.
					 e) You are returned to the highlighted menu screen. Press "b" to Boot the OS.
					 f) You are now in CentOS 6.
			18) Login with "root" password "mediaserver".
			
Configure Media Server -------------------------------------------
			
			19) Install the needed programs to run USB Setup. Type: "yum install perl -y" Press ENTER.
			20) Several Updates will run, after they are complete you will need to create a Directory, mount the Configuration USB Drive, 
				  and run the Media Server Setup.
			21) Change to the root Directory, Type: "cd /" and Press ENTER.
			21) Type: "mkdir /MediaServerTools" and Press ENTER.This will create MediaServerTools. (Ensure to use caps in the right place! NO SPACES.)
			22) After the folder is created we will mount the Drive. Insert the USB Device Labeled "Media Server Setup".
			23) Type: "mount /dev/sdb1 /MediaServerTools". Press ENTER. If all went well, the drive should mount and you wont even notice it.
			24) Almost Done! Type: "perl /MediaServerTools/Setup" and Press ENTER. This will do all the rest of the work for you.
						