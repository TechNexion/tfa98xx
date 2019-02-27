# TFA9892 driver for TechNexion Voicehat


[TechNexion VOICEHAT](https://shop.technexion.com/voicehat.html)

The TFA9892 is a high efficiency class-D audio amplifier with a sophisticated speaker boost and protection algorithm

To make and make install module for TFA98xx driver:

> KDIR=\<your kernel source path> make

> KDIR=\<your kernel source path> INSTALL_MOD_PATH=\<absolute path of kernel module> make modules_install

(NOTE: The "modules" directory should be already installed kernel module inside)


Load the module driver on the board:

> modprobe snd-soc-tfa98xx

* Supported kernel: 4.9.x, 4.14.x
