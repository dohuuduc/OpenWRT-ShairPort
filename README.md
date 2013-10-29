This is a Git Branch for building ShairPort from GIT feed on OpenWrt
Updated by Quentin Smart 

Uses the latest https://github.com/abrasive/shairport version against a 703N on openWRT, works well on attitude adjustment

1. Add "src-git qs git://github.com/sm3rt/OpenWRT-ShairPort.git;master" to feeds.conf
2. scripts/feeds update -a
3. scripts/feeds install shairport_new
4. In make menuconfig ensure that you choose sound shairport_new not multimedia shairport 
   as the later doesn't work well on the 703N

It will install a ShairPort feed that will only need to depend on alsa-lib.

If you've issue with compilation, please raise an issue here.
If it is an issue with playback, please contact the maintainer of ShairPort.
