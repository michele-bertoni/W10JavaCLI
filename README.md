# Installation guide
Author: Michele Bertoni

1. ## Clone repository
	* [Download repository](https://github.com/michele-bertoni/W10JavaCLI/archive/master.zip)
	* Unzip the downloaded archive

2. ## Install Bash on Ubuntu on Windows (BUW)
	* Open Windows PowerShell as Administrator by pressing ```WINDOWS + X``` and then selecting the correct voice
	* Enable the "Windows subsystem for Linux" by running ```Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux```
	* Reboot when asked
	* Install [Ubuntu from Microsoft Store](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
	* Launch the application and set username and password

3. ## Configure BUW
	* Move Ubuntu.lnk on the Desktop
	* Right click on the link, Properties
	* Add your profile name after ```C:\Users\``` (e.g. ```C:\Users\michele```)
	* If the icon is not automatically recognized, manually bind it: it should be in ```W10JavaCLI-master\link\ubuntu.ico```
	* From now on, by pressing ```CTRL + ALT + T``` you will open a new Bash window

4. ## Install Java
	* Download [Java](https://www.java.com/it/download/manual.jsp) for Linux x64
	* Open BUW
	* Browse the download directory (it should be ```cd Downloads```)
	* From now on, I will consider jre version 8u171, if yours is different, please edit the following commands
	* Create the installation directory ```sudo mkdir /usr/java```
	* Move the .tar.gz to the installation directory: ```sudo mv jre-8u171-linux-x64.tar.gz /usr/java/jre-8u171-linux-x64.tar.gz```
	* Install ```sudo tar zxvf jre-8u171-x64.tar.gz```
	* Remove .tar.gz ```sudo rm jre-8u171-linux-x64.tar.gz```
	* Move to Home directory ```cd```
	* Open .bashrc ```nano .bashrc```
	* Add the following lines of code at the end of the file (please remind to eventually change jre directory name):
		```
		# java
		export JAVA_HOME=/usr/java/jre1.8.0_171
		export PATH=${PATH}:${JAVA_HOME}/bin
		```
	* Save changes and close the text editor
	* Close BUW

5. ## Configure correct font
	* Install on Windows the font ```DejaVu Sans Mono for Powerline.ttf``` by double-clicking it and selecting install
	* Open BUW, then right-click the upper header and select Properties
	* Select ```DejaVu Sans Mono for Powerline``` in the Font tab, then apply
	* Repeat this also for Default properties
	* You can also set the same font for IntelliJ IDEA console for easier debugging

6. ## Test
	* Double click on the HanoiTower.bat file (you might need to change jre directory in the .sh file)
	* You should see an auto-solving Hanoi Tower, full colored, where the disks are composed by dice characters
	* If everything is right, the configuration is done
	* You can get inspiration from this test when making the final deployment of your java application
