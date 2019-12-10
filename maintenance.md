# OS maintenance

## Resources
- For CPU and Memory usage: `top` or `htop`.
- For processews `ps aux`

## Disk
```
# This command display memory usage
df -h
# Then you could use du to start debugging how the memory's been used
sudo du -bsh --exclude={/proc,/run,/home} /*
```
You do not need to have more than two/three kernels in your system, so check these directories and remove old ones:
- `/boot/vmlinuz-X.Y`
- `/boot/initramfs-X.Y`
- `/boot/System.map-X.Y`
- `/boot/config-X.Y`
- `/usr/lib/modules/X.Y`
Note: check which kernel you're using with `uname -r`
