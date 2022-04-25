 
## make

```
[root@centos7 bbb-libbsd]# make
  
 ```
 
## run 

```
[root@centos7 bbb-libbsd-cfs]# qemu-system-arm -serial null -serial mon:stdio -nographic   -M xilinx-zynq-a9 -m 256M   -net tap,ifname=qtap,script=no,downscript=no   -net nic,model=cadence_gem,macaddr=0e:b0:ba:5e:ba:12 -kernel rki.elf.pre
qemu-system-arm: warning: nic cadence_gem.1 has no peer


RTEMS Kernel Image With LibBSD Booting


*** RTEMS Info ***
6.0.0.671f126a3a8e6ce5da87aa75c7205fb764e95c78


 BSP Ticks Per Second = 100
*** End RTEMS info ***

Populating Root file system from TAR file.
Setting up filesystems.
nexus0: <RTEMS Nexus device>
cgem0: <Cadence CGEM Gigabit Ethernet Interface> on nexus0
miibus0: <MII bus> on cgem0
e1000phy0: <Marvell 88E1111 Gigabit PHY> PHY 0 on miibus0
e1000phy0:  none, 10baseT, 10baseT-FDX, 100baseTX, 100baseTX-FDX, 1000baseT-FDX, 1000baseT-FDX-master, auto
e1000phy1: <Marvell 88E1111 Gigabit PHY> PHY 23 on miibus0
e1000phy1:  none, 10baseT, 10baseT-FDX, 100baseTX, 100baseTX-FDX, 1000baseT-FDX, 1000baseT-FDX-master, auto
info: cgem0: Ethernet address: 0e:b0:ba:5e:ba:12
arasan_sdhci1: <Zynq-7000 SDHCI> on nexus0
arasan_sdhci0: <Zynq-7000 SDHCI> on nexus0
zy7_slcr0: <Zynq-7000 slcr block> on nexus0
Found first Ethernet interface called cgem0
cgem0: cgem_mediachange: could not set ref clk0 to 25000000.
Starting the FTP Server.
Initializing Local Commands.
Adding Target specific commands
Running /shell-init.

1: mkdir ram
2: mkrfs /dev/rda
3: mount -t rfs /dev/rda /ram
mounted /dev/rda -> /ram
4: hello
    ____  ______________  ________ 
   / __ \/_  __/ ____/  \/  / ___/ 
  / /_/ / / / / __/ / /\_/ /\__ \  
 / _, _/ / / / /___/ /  / /___/ /  
/_/ \_| /_/ /_____/_/  /_//____/   

Hello RTEMS!
Create your own command here!
info: lo0: link state changed to UP
info: cgem0: link state changed to UP
Starting shell....


RTEMS Shell on /dev/console. Use 'help' to list commands.
shell0 [/] # 
```