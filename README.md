# Skelestruder

<https://www.thingiverse.com/thing:2845416>

# Skelestruder firmware patch for MK3 and MK3S

On CentOS 7, install some prerequisites:
`yum install unzip vim-common python3 

To apply this patch:
* `mkdir ~/git && cd ~/git`
* `git clone https://github.com/prusa3d/Prusa-Firmware`
* `git clone https://github.com/soostdijck/skelestruder-patch`
* `cd Prusa-Firmware`
* `git checkout v3.9.2`
* `git apply ../skelestruder-patch/skelestruder-3.9.2.patch`
* Only for MK3S owners:`cp Firmware/variants/1_75mm_MK3S-EINSy10a-E3Dv6full.h Firmware`

# Compile patched firmware

> won't work on a mac without jumping through 100 hoops...

* `./build.sh`

Reset the saved settings on your printer by reloading them from the firmware.
* send M502 
* then M500
to your printer after the update.
