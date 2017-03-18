### Working Sierra on Gigabyte GA-Z77-DS3H

#### My setup:
- Gigabyte GA-Z77-DS3H (bios rev 1.1)
- Intel 3570К Core i5-3570К, 3.4 GHz, 1155, OEM
- Gigabyte NVidia GeForce GT 640, 2048 Mb
- SSD

I have a lot of problems when upgrade from El Capitan to Sierra, wake up from sleep doesn't work and finally I clear my SDD and reinstall Sierra and have another problems:
- reboots on sleep
- sleep and immediately wake up
- ethernet doesn't work
- sound doesn't work

After numerous attempts finally I get worked Sierra, **all problems solved: sleep, sound, wake up- work fine**


So I'd like to share with you my custom set of kext and config (config hasn't mush affection, main problem in get needed kext)

### My clover and kext setup:

- [Clover config file](./EFI/CLOVER/config.plist) (In `config.plist` notice that there 3 fields with _REPLACE WITH YOURS_)
- [List of kext in S/L/E](./Extensions/readmeSLE.md) (System/Library/Extensions)
- [Some not standard kext in S/L/E](./Extensions/SLE/) (System/Library/Extensions)
- [List of kext in L/E](./Extensions/readmeLE.md) (Library/Extensions)
- [Kext in Clover](./EFI/CLOVER/kexts/10.12/)

#### [Download all](https://github.com/pcherednichenko/hackintoshZ77/archive/master.zip)

I install Sierra by UniBeast and after intall Multibeast with `System Definitions` as iMac13,2

To make sound work I use [audio_cloverALC-120_v1.0d.command](./audio_cloverALC-120_v1.0d.command) with default setup options (yes, yes, yes as I remember)

I hope with this configuration you will get to make Sierra work fine

#### What I was trying to do::
- add or remove AtherosL1cEthernet.kext (ethernet or sleep doesn't work)
- use AtherosE2200Ethernet.kext (sleep doesn't work)
- try solution from [this post](https://www.tonymacx86.com/threads/unibeast-6-0-works-fine-but-no-ethernet-after-post-installation-ga-z77-ds3h-core-i5-3570k-gtx.174036/#post-1113204) (once I start getting Kernel Panic)
