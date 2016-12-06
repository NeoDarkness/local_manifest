Cyanogenmod For Galaxy Grand Prime
==================================

Instructions
---------------

To get started with CyanogenMod, you'll need to get familiar with
[Git and Repo](http://source.android.com/download/using-repo).

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/cm-14.1

Next, naviate into that new directory via the terminal:

	cd ~/cm-14.1

To initialize your local repository using the Turbo ROM trees, use this command:

	repo init -u git://github.com/CyanogenMod/android.git -b cm-14.1

Also add the local manifests:

	git clone https://github.com/CarlosArriagaCM/local_manifest -b cm-14.1 .repo/local_manifests

Then sync up with this command:

	repo sync -fcj4 --force-sync --force-broken
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/cm-14.1

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ ~/cm-14.1/prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	brunch fortuna3g or brunch fortunave3g
