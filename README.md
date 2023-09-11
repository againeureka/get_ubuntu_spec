# Get Ubuntu Spec.

- List of commands to check Ubuntu system specifications
- J. Park @ 2023

--------------------------------
## CPU

- All CPU Info

```bash
$ cat /proc/cpuinfo
 ```

- Number of physical CPU cores

```bash
$ cat /proc/cpuinfo | grep processor | wc -l
```

- Number of logical CPU cores

```bash
$ grep -c processor /proc/cpuinfo
```

- Number of CPUs

```bash
$ grep "physical id" /proc/cpuinfo | sort -u | wc -l
```

- Number of cores per 1 CPU

```bash
$ grep "cpu cores" /proc/cpuinfo | tail -1
```

--------------------------------
## Memory

- All
  
```bash
$ cat /proc/meminfo
```

- Total Memory

```bash
$ cat /proc/meminfo | grep MemTotal
```


--------------------------------
## GPU

- VGA
  
```bash
$ lspci | grep -i VGA
```

- with nvidia-smi

```bash
$ nvidia-smi --query | fgrep 'Product Name'
```



--------------------------------
## Disk

- All disks

```bash
$ sudo fdisk -l
```

- SSD

```bash
$ sudo fdisk -l | grep SSD
```

- Tera Bytes Disks

```bash
$ sudo fdisk -l | grep TiB
```


--------------------------------
## Network

- Port
  
```bash
$ sudo netstat -ap
```

- Network Monitoring

```bash
$ bmon
```
