###Kernel-3.10 Source for s823_s63(MT6582) 

		sudo apt-get install ccache
		sudo gedit ~/.bashrc
Add:

		export USE_CCACHE=1
		export CCACHE_DIR=~/android/.ccache

Build:

		sudo chmod -R 777 * ~/s823_s63-3.10/arm-eabi-4.8
		cd ~/s823_s63-3.10/kernel
		export ARCH=arm && export ARCH_MTK_PLATFORM=mt6582 && export CROSS_COMPILE=~/s823_s63-3.10/arm-eabi-4.8/bin/arm-eabi-
		make clean
		make s823_s63_defconfig
		./build.sh


