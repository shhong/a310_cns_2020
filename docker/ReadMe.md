# Installing NEURON via docker

1. Install [Docker Community Edition](https://hub.docker.com/search/?type=edition&offering=community).

2. [Turn on drive sharing](https://blogs.msdn.microsoft.com/wael-kdouh/2017/06/26/enabling-drive-sharing-with-docker-for-windows/) if you use Windows.

3. Start Docker.

4. Create an empty directory that you will use for the class and go to it.

5. Download a docker image by entering the following command in a terminal (PowerShell in Windows). **The docker image is as big as ~5GB**, and please make sure that you have sufficient space in your computer.
   ```shell
   docker pull shhongoist/a310_cns_2020
   ```

5. Run the following command (please make sure you enter the whole thing, until "...a310_cns_2020")
   ```shell
   docker run -it -p 8889:8889 -p 6901:6901 -e VNC_RESOLUTION=1024x768 -v ${PWD}:/root/Documents shhongoist/a310_cns_2020
   ```

   This will start a virtual linux environment, which will give you a shell prompt as

   ```shell
   root@83d0e4956e42:~/Documents#
   ```

   as you are in a directory `/root/Documents`. If drive sharing is correctly configured, this should be linked to the directory that you launched this linux environment.

6. Now open the following address in a web browser

   http://0.0.0.0:8889

   This will open a jupyter lab environment.

7. It also starts a VNC server, which will give you access to the virtual desktop. Open http://0.0.0.0:6901/vnc_auto.html?password=vncpassword in a web browser.


##  Additional notes

1. The size of the desktop is 1024x768. If you want to change this, change `VNC_RESOLUTION=1024x768` in the starting command to whichever size you want.
2. In some systems, `0.0.0.0` may not be accessible. In this case replace `0.0.0.0` by `localhost`.

---
_Written by Sungho Hong, Computational Neuroscience Unit, Okinawa Institutes of Science and Technology_

_January 2020_

