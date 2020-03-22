LineageOS For Xiaomi Redmi Note 4/4X
======================================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/pixel

Next, naviate into that new directory via the terminal:

	cd ~/pixel

To initialize your local repository using the Turbo ROM trees, use this command:

	repo init -u https://github.com/PixelExperience/manifest -b pie

Also add the local manifests:

	git clone https://github.com/NeoDarkness/local_manifest -b mido-pie .repo/local_manifests

Then sync up with this command:

	repo sync --force-sync
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/pixel

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	lunch aosp_mido-userdebug
	mka bacon -jX
