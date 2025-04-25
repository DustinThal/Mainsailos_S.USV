# Mainsailos_S.USV
getting s.usv from Olmatic to work under MainsailOS


To get everything up and running smoothly, I followed these steps with the latest RaspberryMatic version 3.81.5.20250326:

1. Installed and tested my s.usv advanced mobil to ensure it works properly (and it does!).
2. Copied the files `/lib/ld-linux-armhf.so.3` and `/lib/libc.so.6` from RaspberryMatic to MainsailOS, placing them in the same directory (`/usr/lib/`).
3. Set permissions to allow execution with `chmod 0777`.
4. Created a symbolic link with `sudo ln -s /lib/ld-linux-armhf.so.3 /lib/ld-linux.so.3`, following advice from [this forum post](https://forums.raspberrypi.com/viewtopic.php?t=369895#p2219402).
5. (Installed `susvd-en-2.33-systemd-all.deb`.)
6. Finally, copied the files from `/opt/susvd` on RaspberryMatic to the corresponding directory on MainsailOS.

These steps may have included some unnecessary details, but following this process got everything working smoothly for me.
