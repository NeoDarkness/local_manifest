LineageOS For Xiaomi Redmi 2/Prime/Pro
======================================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/lineage

Next, naviate into that new directory via the terminal:

	cd ~/lineage

To initialize your local repository using the Turbo ROM trees, use this command:

	repo init -u git://github.com/LineageOS/android.git -b cm-14.1

Also add the local manifests:

	git clone https://github.com/NeoDarkness/local_manifest -b cm-14.1-xiaomi .repo/local_manifests

Then sync up with this command:

	repo sync --force-sync
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/lineage

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	brunch wt88047
