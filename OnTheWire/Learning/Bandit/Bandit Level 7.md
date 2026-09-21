password = pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

i entered the system server but i cant any directory in the bandit directory so with hint it mentioned that it can be any where in server so we need to use / -root search

and we got some hint 
1. owned by user bandit7
2. owned by group bandit6
3. 33 bytes in size

so we can search using
find / -type f -user bandit7 ---> for who owned in the user 
find / -type f -group bandit6 ---> for who owned in the group
find / -type f -size 33c ---> find using size

so we combine all 
`find / -type f -user bandit7 -group bandit6 -size 33c`


bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c
find: ‘/snap’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/manpage/manpage3-pw’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/run/pam_pidns’: Permission denied
find: ‘/run/udisks2’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11017’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/5011’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/5004’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/user/8005’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/13003’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit0’: Permission denied
find: ‘/run/screen/S-behemoth1’: Permission denied
find: ‘/run/screen/S-bandit18’: Permission denied
find: ‘/run/screen/S-bandit13’: Permission denied
find: ‘/run/screen/S-bandit14’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-narnia0’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit19’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/cloud-init/share’: Permission denied
find: ‘/run/credentials/serial-getty@ttyS0.service’: Permission denied
find: ‘/run/credentials/getty@tty1.service’: Permission denied
find: ‘/run/credentials/systemd-networkd.service’: Permission denied
find: ‘/run/credentials/systemd-resolved.service’: Permission denied
find: ‘/run/credentials/systemd-journald.service’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/cache/apparmor/147ee081.0’: Permission denied
find: ‘/var/cache/apparmor/ae1a4050.0’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/etc/xinetd.d’: Permission denied
find: ‘/etc/credstore.encrypted’: Permission denied
find: ‘/etc/credstore’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/stunnel’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/2/task/2/fd’: Permission denied
find: ‘/proc/2/task/2/fdinfo’: Permission denied
find: ‘/proc/2/task/2/ns’: Permission denied
find: ‘/proc/2/fd’: Permission denied
find: ‘/proc/2/map_files’: Permission denied
find: ‘/proc/2/fdinfo’: Permission denied
find: ‘/proc/2/ns’: Permission denied
find: ‘/proc/46/task/46/fdinfo/6’: No such file or directory
find: ‘/proc/46/fdinfo/5’: No such file or directory
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/leviathan0/.backup’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/leviathan4/.trash’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/root’: Permission denied
find: ‘/sys/kernel/tracing/osnoise’: Permission denied
find: ‘/sys/kernel/tracing/hwlat_detector’: Permission denied
find: ‘/sys/kernel/tracing/instances’: Permission denied
find: ‘/sys/kernel/tracing/trace_stat’: Permission denied
find: ‘/sys/kernel/tracing/per_cpu’: Permission denied
find: ‘/sys/kernel/tracing/options’: Permission denied
find: ‘/sys/kernel/tracing/rv’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/tmp’: Permission denied

so it fucked up by many permission denied errors so we throw thoese error to our black hole

`find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null`

bandit6@bandit:~$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password

we fond the location now fucking open it

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

Found password

LEVEL DONE