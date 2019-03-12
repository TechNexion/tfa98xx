# TFA9892 driver for TechNexion Voicehat

* Supported kernel: 4.9.x, 4.14.x

[TechNexion VOICEHAT](https://shop.technexion.com/voicehat.html)

The TFA9892 is a high efficiency class-D audio amplifier with a sophisticated speaker boost and protection algorithm


## Prepare firmware files

This codec driver requires firmware.
Please download it from NXP codeaurora:

[TFA9892N1A_stereo_32FS.cnt](https://source.codeaurora.org/external/imxsupport/meta-avs-demos/plain/recipes-kernel/tfa98xx/files/TFA9892N1A_stereo_32FS.cnt?h=imx-alexa-sdk)

Place the firmware file in the following path on the target board:

> /lib/firmware/tfa98/9912/TFA9892N1A_stereo_32FS.cnt

> ln -sf /lib/firmware/tfa98/9912/TFA9892N1A_stereo_32FS.cnt /lib/firmware/tfa98xx.cnt

Codec driver will look for firmware under /lib/firmware/tfa98xx.cnt

## Complile
To make and make install module for TFA98xx driver:

> KDIR=\<your kernel source path> make

> KDIR=\<your kernel source path> INSTALL_MOD_PATH=\<absolute path of kernel module> make modules_install

(NOTE: The "modules" directory should be already installed kernel module inside)

## Load module driver

Load the module driver on the board:

> modprobe snd-soc-tfa98xx
