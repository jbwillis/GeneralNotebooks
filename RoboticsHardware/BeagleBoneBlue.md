# BeagleBone Blue
The BeagleBone Blue (BBB) is a robotics-specific model of the BeagleBone Black embedded linux computer. It adds motor controllers, 2-cell LiPo battery management, WiFi, an MPU9250 IMU, a Baro, servo outputs, and more! 

## Key notes
* IP Address:
  * `192.168.6.1` or `192.168.7.1`
  * This should show up when you plug the board into a USB port on a computer
* Default username and password
  * Username: `debian`
  * Password: `temppwd`

## Robot Control (RC) Examples
The BBB has a bunch of executables on it that start with `rc_*`. These are small example programs for testing different features in the robot control library and on the board. The [online documentation](http://strawsondesign.com/docs/librobotcontrol/examples.html) provides some information on how these programs operate, and some of the programs have a `-h` option for seeing what arguments they expect to recieve.

## Disk space and the SD card
The BBB has a linux image preinstalled on it. From examining the output of `df` it appears that the linux image takes up approximately 1.5GB of the total 4GB available on the onboard memory. I have loaded the latest Debian image onto an SD card and booted it ([see the getting started page](http://beagleboard.org/getting-started)), but it seems that there are some differences between the image on the onboard memory and the image on the SD card, as I was unable to test the servo outputs using the SD card image.

