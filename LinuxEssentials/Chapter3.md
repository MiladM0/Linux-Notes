# 📖 Chapter 03: Investigating Linux's Principles and Philosophy

> [!NOTE]
> This chapter is mostly historical and conceptual. It is useful for understanding Linux's background and philosophy, but contains less technical material than previous chapters.

---

# 🕰️ Linux Through the Ages

## Linux's Origins

### 1991: The Birth of Linux

* Linux was created in **1991**.
* It started as a personal project by **Linus Torvalds**.
* According to Linus, it began as a project "just for fun."

---

## The Computing World of the Early 1990s

### 💻 x86 Computers

The dominant personal computers were based on the **x86 architecture**.

> [!TIP]
> x86 refers to the CPU family (Intel 8086 and descendants), not specifically to 32-bit systems.

---

### 📀 MS-DOS

Most personal computers ran **MS-DOS**.

Characteristics:

* Single-user
* Single-tasking
* Relatively simple

---

### 🖥️ Unix

Unix was already widely used on larger systems.

Characteristics:

* Multi-user
* Multitasking
* More sophisticated than MS-DOS

---

## 👨‍💻 Linus Torvalds

* Student at the University of Helsinki
* Interested in Unix-like systems
* Started developing what would eventually become Linux

---

## The First Linux Project

Initially, Linux was developed as a:

```text
Terminal Emulator
```

Its purpose was to connect to larger Unix systems.

Over time, the project evolved into:

```text
Unix-Compatible Kernel
```

---

## Unix Compatibility

Linux was designed to be compatible with Unix concepts and software.

> [!IMPORTANT]
> Linux is not Unix itself. It is a Unix-like operating system.

Because of this compatibility, many Unix programs could be adapted to run on Linux.

---

## Historical Impact

Many technologies from the early 1990s continue to influence modern computing.

> We are built atop the foundation that was created in the past.

Examples:

* Unix philosophy
* TCP/IP networking
* Command-line tools
* Open-source development

---

## AT&T and Unix

AT&T developed Unix but faced legal and business restrictions that limited its commercialization.

This created opportunities for alternative Unix-like systems, including Linux.

---

## Growth of Linux

As Linux gained popularity:

* Programmers began writing software for Linux.
* Linux became a favorite operating system on x86 hardware.
* Communities formed around Linux development.

---

## Early Linux Distributions

Several Linux distributions appeared during the 1990s.

Some still exist today:

| Distribution | Status       |
| ------------ | ------------ |
| Red Hat      | Still active |
| Slackware    | Still active |
| Debian       | Still active |

---

# ⚙️ Linux Kernel Design

Linux uses a:

```text
Monolithic Kernel
```

### Monolithic Kernel

Most core operating system services run inside kernel space.

Examples:

* Memory management
* Process management
* Device drivers
* File systems
* Networking

> [!NOTE]
> Monolithic kernels generally provide high performance because components communicate directly inside the kernel.

---

# 🔓 Advantages of Open Source Software

Compared with closed-source software, open-source software offers several advantages.

---

## ✅ Better Code

Source code is publicly available.

This means developers can:

* Review code
* Audit code
* Improve code
* Fix bugs

---

## ✅ More Flexibility

Users can customize software for their own requirements.

Examples:

* Adding features
* Removing unwanted features
* Adapting software to special environments

---

## ✅ Lower Cost

Many open-source projects are available at no cost.

Benefits include:

* Reduced licensing fees
* Lower deployment costs
* Easier experimentation

---

## ✅ Lack of Vendor Lock-in

Users are less dependent on a single company.

Benefits include:

* Greater control over data
* Long-term accessibility
* Alternative support options

> [!TIP]
> Even proprietary file formats and protocols are often reverse-engineered by open-source communities.

---

# 🖥️ Understanding Operating System Roles

Operating systems serve different types of computers.

---

## 1️⃣ Embedded Computers

Embedded systems are specialized computers designed for specific tasks.

### Examples

* 📱 Mobile Phones

  * Android
  * Tizen
  * Ubuntu Touch

* 📚 E-book Readers

* 📺 DVR Systems

  * TiVo

* 🚗 Automotive Systems

  * GPS Navigation
  * Vehicle Control Systems

* 🏠 Smart Appliances

  * Televisions
  * Refrigerators

---

## 2️⃣ Desktop & Laptop Computers

General-purpose personal computers.

### Examples

* Desktop PCs
* Laptops
* Tablets

---

## 3️⃣ Server Computers

Servers provide services to other computers over a network.

### Common Server Types

* 🌐 Web Server
* 📧 Email Server
* 🧭 DNS Server
* 📡 DHCP Server
* 🗄️ Database Server
* 🖨️ Print Server
* 📁 File Server

---

# 👀 Famous Open Source Quote

> [!IMPORTANT]
> "Given enough eyeballs, all bugs are shallow."

This idea suggests that when many people can inspect source code, bugs become easier to find and fix.

This principle is often associated with open-source development.

---

# 📝 Quiz & Review Notes

## 1️⃣ Main Difference Between FreeBSD and Linux

| Linux                                   | FreeBSD                                 |
| --------------------------------------- | --------------------------------------- |
| Kernel only                             | Complete operating system               |
| Usually combined with GNU tools         | Includes its own userland and utilities |
| Distributed through Linux distributions | Distributed as a complete OS            |

### Linux

Linux provides:

* Kernel
* Foundation for distributions

Examples:

* Ubuntu
* Fedora
* Debian

---

### FreeBSD

FreeBSD provides:

* Kernel
* Utilities
* Userland tools

All developed as a more integrated operating system.

> [!NOTE]
> FreeBSD and Linux also differ in licensing, architecture, and development models.

---

## 2️⃣ BSD Variants Used Today

### FreeBSD

✅ Most popular BSD

✅ Performance-focused

✅ Feature-rich

---

### OpenBSD

✅ Security-focused

✅ Strong security reputation

---

### NetBSD

✅ Portability-focused

✅ Runs on many hardware platforms

---

### DragonFly BSD

✅ Scalability-focused

---

### TrueOS (Formerly PC-BSD)

✅ User-friendly FreeBSD derivative

---

## 3️⃣ Linux vs Unix

| Unix                        | Linux                      |
| --------------------------- | -------------------------- |
| Original operating system   | Unix-like operating system |
| Developed at AT&T Bell Labs | Created by Linus Torvalds  |
| Proprietary                 | Open source                |
| Originated in the 1970s     | Released in 1991           |

> [!IMPORTANT]
> Linux is not Unix.
>
> Linux is a Unix-like operating system inspired by Unix concepts and behavior.

---

## 4️⃣ x86 vs 32-bit

These terms describe different things.

### x86

Refers to:

```text
CPU Architecture Family
```

Examples:

* Intel 8086
* Intel 80386
* Modern x86 processors

---

### 32-bit

Refers to:

```text
Data Width
```

Meaning:

* How much data a CPU processes at once
* Address size
* Register size

---

### Relationship

An x86 processor may be:

* 16-bit
* 32-bit
* 64-bit

Examples:

| Term         | Meaning                 |
| ------------ | ----------------------- |
| x86          | CPU architecture family |
| x86 (32-bit) | 32-bit x86 processor    |
| x86-64       | 64-bit x86 processor    |

> [!TIP]
> x86 describes the processor family, while 32-bit describes its operating width.

---

# 📌 Key Takeaways

* Linux was created by Linus Torvalds in 1991.
* Linux started as a personal project and evolved into a Unix-compatible kernel.
* Linux uses a monolithic kernel architecture.
* Open-source software offers transparency, flexibility, lower cost, and freedom from vendor lock-in.
* Operating systems power embedded devices, desktops, laptops, and servers.
* Linux is a kernel; FreeBSD is a complete operating system.
* Linux is Unix-like but is not Unix.
* x86 refers to an architecture family, while 32-bit refers to data width.

---
