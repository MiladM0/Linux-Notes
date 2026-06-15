# 🖥️ Computer Hardware, Storage & Linux Filesystems

---

# 🧠 CPU Families (Desktop Processors)

## x86

The **x86 architecture** originated from Intel's 8086 processor family.

### Historical Evolution

```text
8086 → 80286 → 80386 → 80486 → Pentium → Core Series
```

### Characteristics

* Originally a 16-bit architecture
* The **80386 (386)** introduced 32-bit computing
* Became the dominant desktop CPU architecture

### Compatible Manufacturers

* Intel
* AMD
* Cyrix
* VIA

### Example AMD CPUs

* Athlon
* Duron

> [!NOTE]
> The earliest x86 processors were 16-bit. The 80386 was the first widely used 32-bit x86 processor.

---

## x86-64

Also known as:

* AMD64
* Intel 64

### Characteristics

* 64-bit extension of x86
* Backward compatible with 32-bit software
* Dominant desktop/server architecture today

### Examples

* Intel Core i3
* Intel Core i5
* Intel Core i7
* AMD Ryzen series

> [!TIP]
> Most modern Linux distributions support both 64-bit and legacy 32-bit applications on x86-64 systems.

---

## ARM Processors

ARM processors dominate the mobile and embedded markets.

### Characteristics

* RISC (Reduced Instruction Set Computing) architecture
* High power efficiency
* Common in smartphones and tablets

### Examples

* Apple Silicon
* Qualcomm Snapdragon
* Samsung Exynos
* Raspberry Pi CPUs

> [!NOTE]
> Modern Linux distributions run very well on ARM systems.

---

# 🔢 CPU Bit Depth

Computers process information in binary:

```text
0 and 1
```

Bit depth affects:

* Memory addressing
* Data processing capacity
* Maximum usable RAM

---

## 32-bit CPUs

Maximum address space:

2^{32}=4,294,967,296

This corresponds to approximately:

```text
4 GiB of addressable memory
```

> [!IMPORTANT]
> A typical 32-bit CPU can directly address approximately 4 GiB of memory.

---

## Why Larger Bit Depth Matters

Benefits include:

* Larger memory support
* Larger address spaces
* Better performance for certain workloads

---

# 🖥️ Understanding Motherboards

The motherboard acts as the computer's central communication platform.

> [!NOTE]
> The motherboard is often compared to the computer's nervous system.

---

## Main Components

### Chipsets

Chipsets control communication between hardware components.

Examples:

* Storage interfaces
* USB controllers
* Network interfaces
* Expansion devices

---

## Expansion Slots & Connectors

### CPU Socket

Holds the processor.

### RAM Slots

Hold memory modules.

### Storage Connectors

* SATA
* M.2
* (Historically) PATA

### External Connectors

* USB ports
* Audio ports
* Ethernet ports
* Display outputs

---

## Motherboard Form Factors

Different systems require different motherboard sizes.

Examples:

* Desktop
* Server
* Laptop
* Mini-PC

---

## Historical Chipset Design

Older systems commonly used:

### Northbridge

Managed:

* CPU communication
* Memory controller
* Graphics

### Southbridge

Managed:

* USB
* SATA
* Audio
* Other peripherals

> [!NOTE]
> Modern CPUs integrate many Northbridge functions directly into the processor.

---

# ⚡ Power Supplies (PSU)

A Power Supply Unit converts:

```text
AC → DC
```

### Responsibilities

* Deliver power to system components
* Provide stable voltages
* Protect against power issues

---

## Important Considerations

### Power-Hungry Devices

Examples:

* GPUs
* CPUs
* Storage arrays

### Wattage

Always verify:

```text
PSU Output Watts
```

before purchasing components.

---

# 💾 Disk Interfaces

## PATA (Parallel ATA)

Also known as:

* IDE
* EIDE

### Characteristics

* Older technology
* 40-pin or 80-conductor ribbon cables
* Multiple devices per cable

### Related Standard

ATAPI enabled ATA controllers to support:

* CD-ROM drives
* DVD drives
* Other devices beyond hard disks

---

## SATA (Serial ATA)

Introduced in:

```text
2003
```

### Advantages

✅ Smaller cables

✅ Better airflow

✅ Simpler connections

### Characteristics

* One drive per cable

### External Version

```text
eSATA
```

---

## SCSI

### Small Computer System Interface

Historically common in servers.

### Modern Variant

```text
SAS
(Serial Attached SCSI)
```

Widely used in enterprise environments.

---

# 🧩 Partitioning Schemes

## MBR (Master Boot Record)

Traditional partitioning system used by BIOS-based PCs.

Also known as:

```text
MS-DOS Partition Table
```

---

### Primary Partitions

* Simplest partition type
* Maximum of 4

---

### Extended Partition

Special partition that acts as a container.

Rules:

* Only one per disk
* Holds logical partitions

---

### Logical Partitions

Created inside an extended partition.

Benefits:

* More than four partitions possible

---

# ⚖️ MBR vs GPT

## MBR

### Advantages

* Very old and widely supported

### Limitations

* Maximum 4 primary partitions
* Maximum disk size ≈ 2 TiB

---

## GPT (GUID Partition Table)

Modern replacement for MBR.

### Advantages

* Supports up to 128 partitions
* Supports extremely large disks
* Better redundancy and reliability

### Capacity

Approximately:

```text
8 ZiB
(Zebibytes)
```

---

### GPT Simplification

GPT does not use:

* Primary partitions
* Extended partitions
* Logical partitions

---

## Linux & Windows Compatibility

### Windows

| Boot Mode | GPT Support   |
| --------- | ------------- |
| BIOS      | ❌ Cannot boot |
| UEFI      | ✅ Supported   |

### Linux

* Supports both MBR and GPT
* Supports BIOS and UEFI

> [!WARNING]
> Be careful when configuring dual-boot systems with Windows and Linux.

---

# 🔧 Linux Partitioning Tools

## fdisk Family

Tools:

* fdisk
* cfdisk
* sfdisk

### Characteristics

* Text-based
* Primarily for MBR disks
* Useful for recovery operations

---

## GNU Parted / GParted

Based on:

```text
libparted
```

### Features

* Supports MBR
* Supports GPT
* Supports many partition table formats

### Interfaces

| Tool    | Interface |
| ------- | --------- |
| Parted  | Text      |
| GParted | GUI       |

---

## GPT fdisk

Tools:

* gdisk
* cgdisk
* sgdisk

### Characteristics

* GPT-focused
* Similar to fdisk
* Advanced GPT management

---

# 📂 What Is a Filesystem?

A filesystem is a data structure used to organize:

* Files
* Directories
* Metadata

---

## Windows Filesystem Layout

Uses drive letters:

```text
C:
D:
E:
```

Typically:

```text
C:
```

is the primary system partition.

---

## Linux Filesystem Layout

Linux uses a single directory tree.

Root directory:

```text
/
```

Additional filesystems are attached using:

```text
Mount Points
```

---

# 🐧 Common Linux Filesystems

## ext2

### Characteristics

* Popular during the 1990s
* No journaling

### Limitation

Longer recovery times after crashes.

---

## ext3

### Characteristics

* ext2 + journaling
* Popular during the 2000s

### Capacity

Up to approximately:

```text
2 TiB
```

---

## ext4

### Characteristics

* Current mainstream Linux filesystem
* Improved performance
* Larger file support
* Journaling

### Capacity

Filesystem sizes can reach far beyond 16 TiB on modern kernels.

> [!TIP]
> ext4 remains the default filesystem for many Linux distributions.

---

## ReiserFS

### Characteristics

* Efficient storage usage
* Similar goals to ext3

> [!WARNING]
> Largely obsolete today.

---

## JFS

Developed by:

```text
IBM
```

Originally for:

```text
AIX
```

---

## XFS

Developed by:

```text
Silicon Graphics (SGI)
```

### Strengths

* Very large files
* Large storage arrays
* Media storage
* Backup servers

---

## Btrfs

Pronounced:

```text
Butter FS
```

or

```text
Better FS
```

### Features

✅ Snapshots

✅ Checksums

✅ Multiple-device support

✅ Advanced volume management

### Capacity

Supports extremely large filesystems (up to EiB scale).

---

## FAT

### Characteristics

* Legacy DOS/Windows filesystem
* Excellent compatibility

### Linux Variants

* msdos
* vfat

### Common Usage

USB flash drives.

---

## ZFS

Developed by:

```text
Sun Microsystems
```

### Features

* Enterprise storage
* RAID support
* Snapshots
* Data integrity verification

---

## NTFS

### Characteristics

* Default Windows filesystem
* Supports permissions and large files

---

## HFS / HFS+

### Apple Filesystems

| Filesystem | Description          |
| ---------- | -------------------- |
| HFS        | Older Mac filesystem |
| HFS+       | Mac OS Extended      |

> [!NOTE]
> Modern macOS primarily uses APFS.

---

## Optical Disc Filesystems

### ISO-9660

Used for:

* CD-ROM
* CD-R

Variants:

* Joliet
* Rock Ridge

---

### UDF

Used for:

* DVD
* Blu-ray

Successor to ISO-9660.

---

# 🖼️ Display Modes & X Window System

## Display Modes

### Text Mode

Command-line interface.

### GUI Mode

Graphical user interface.

---

## Responsibilities of X

Historically, X handled:

* Display initialization
* Resolution management
* Window management support
* Pointer movement
* Keyboard input routing
* Graphics rendering

Additional components:

| Component      | Purpose                      |
| -------------- | ---------------------------- |
| Window Manager | Window movement and resizing |
| Widget Toolkit | Menus, buttons, scroll bars  |
| Xft            | Font rendering               |

> [!NOTE]
> Modern Linux systems perform much of this configuration automatically.

---

## Wayland

Wayland is the modern successor to X11.

### Goals

* Simpler design
* Better security
* Better performance

### Current Status

Most major Linux distributions are moving toward Wayland as the default display protocol.

---

# 🖥️ Display Hardware

## Common Video Connectors

| Connector | Pins     |
| --------- | -------- |
| VGA       | 15       |
| DVI       | Up to 29 |
| HDMI      | 19       |

---

## Monitor Resolution

Resolution = Horizontal Pixels × Vertical Pixels

Examples:

```text
640 × 480
1280 × 1024
1366 × 768
1920 × 1080
2560 × 1440
3840 × 2160
```

> [!TIP]
> Linux usually detects monitor resolution automatically.

---

# 🔌 Device Drivers

## What Is a Driver?

A driver acts as a translator between:

```text
Operating System ↔ Hardware
```

---

## Driver Locations

Drivers may exist:

### Inside the Kernel

Most Linux drivers.

### User Space

Examples:

* SANE
* Ghostscript
* X/Wayland-related components

---

## When Are Manual Drivers Needed?

### Very New Hardware

Kernel may not yet include support.

### Unusual Hardware

Specialized equipment.

### Proprietary Drivers

Examples:

* NVIDIA drivers

### Bug Fixes

May require:

* Driver updates
* Kernel patches

---

# 🛠️ Useful Linux Hardware Commands

## ``` uname -a ```

Displays:

* Kernel version
* Hostname
* Architecture
* System information

---

## ``` lscpu ```

Displays detailed CPU information.

Examples:

* CPU model
* Core count
* Architecture

---

## ``` cat /proc/cpuinfo ```

Shows detailed processor information from the Linux kernel.

---

## ``` lspci ```

Lists PCI devices.

Examples:

* GPU
* Network card
* Audio controller

---

## ``` lsblk -f ```

Displays:

* Block devices
* Partitions
* Filesystem types
* UUIDs

---

## ``` fdisk -l ```

Lists:

* Disks
* Partitions
* Partition tables

Useful for storage troubleshooting.

---

# 📌 Key Takeaways

* x86 and x86-64 dominate desktop computing.
* ARM dominates mobile and embedded systems.
* GPT is the modern replacement for MBR.
* Linux supports many filesystems, including ext4, XFS, Btrfs, and ZFS.
* Wayland is gradually replacing X11.
* Device drivers allow Linux to communicate with hardware.
* Commands such as `lscpu`, `lsblk`, and `lspci` are essential for system inspection.
