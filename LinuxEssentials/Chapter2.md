
# 📖 Chapter 02 : Understanding Software Licensing & Open Source
> [!NOTE]
> Software is considered intellectual property and is protected by copyright laws.

---

## 🏷️ What Is a Software License?

A **software license** is a set of rules that defines how software may be:

* Used
* Copied
* Modified
* Distributed (redistributed)

Without a license, users generally do not have permission to copy or modify software.

---

## 📋 Why Licensing Matters

Every time software is used, copies of it are created.

### Examples of Software Copies

1. Copying a program from installation media to a hard drive or SSD.
2. Loading a program from storage into RAM.
3. Copying RAM contents into swap space.
4. Copying data into CPU or motherboard caches for performance.
5. Creating backups of the software on storage devices.

> [!TIP]
> Because software is constantly being copied during normal operation, licensing determines whether these copies are legally permitted.

---

## 🌐 Organizations Related to Open Source Licensing

| Organization | Full Name                | Purpose                              |
| ------------ | ------------------------ | ------------------------------------ |
| FSF          | Free Software Foundation | Promotes software freedom            |
| OSI          | Open Source Initiative   | Maintains Open Source Definition     |
| CC           | Creative Commons         | Provides licenses for creative works |

---

## 📂 License Files

Open-source software often includes its license text in a file named:

```text
COPYING
```

Other common names include:

```text
LICENSE
LICENSE.txt
COPYRIGHT
```

---

# 🐧 Free Software Foundation (FSF)

The **Free Software Foundation (FSF)** was founded to promote software freedom.

### Key Ideas

✅ Free software

✅ Sharing information

✅ User freedom

✅ Access to source code

### Common License

* GPL (GNU General Public License)

### Four Essential Freedoms

Users should be able to:

1. Run the program.
2. Study how it works.
3. Modify the program.
4. Share copies and improvements.

> [!IMPORTANT]
> In the FSF philosophy, "free" refers to **freedom**, not necessarily price.

---

# 🔓 Open Source Initiative (OSI)

The **Open Source Initiative (OSI)** focuses on defining and promoting open-source software.

### Characteristics

✅ Source code available

✅ Redistribution allowed

✅ Modification allowed

✅ Multiple approved licenses

### Common Licenses

* GPL
* LGPL
* MIT
* BSD
* Apache

### Additional Notes

* Software may be free or paid.
* Commercial use is generally allowed.
* Proprietary software can sometimes coexist with open-source software depending on the license.

---

## ⚖️ FSF vs OSI

| FSF                         | OSI                                |
| --------------------------- | ---------------------------------- |
| Focuses on software freedom | Focuses on open-source development |
| Emphasizes user rights      | Emphasizes practical collaboration |
| Strong support for GPL      | Supports many license types        |
| Philosophical approach      | Development-oriented approach      |

---

# 📜 Common Open Source Licenses

## GNU GPL (General Public License)

### Characteristics

✅ Source code must remain available

✅ Modifications must remain open source

✅ Derived works must use the GPL

> [!WARNING]
> GPL is considered a "copyleft" license because derivative works must also remain open source.

---

## GNU LGPL (Lesser GPL)

### Characteristics

✅ Similar to GPL

✅ More flexible

✅ Commonly used for libraries

Allows proprietary software to link against LGPL libraries under certain conditions.

---

## BSD License

### Characteristics

✅ Very permissive

✅ Minimal restrictions

✅ Can be used in proprietary software

---

## MIT License

### Characteristics

✅ Simple

✅ Short

✅ Highly permissive

✅ Popular for modern projects

---

## Apache License

### Characteristics

✅ Permissive

✅ Includes patent protection

✅ Common in enterprise software

---

## Artistic License

### Characteristics

✅ Flexible licensing model

✅ Often associated with Perl projects

---

## 🏢 Linux Industry Example

Historically:

```text
Red Hat Enterprise Linux (RHEL)
           ↓
        CentOS
```

CentOS was built from Red Hat Enterprise Linux source packages and provided a community-supported alternative.

---

# 📌 Key Takeaways

* Software is intellectual property.
* A software license defines how software can be used, copied, modified, and distributed.
* Open-source software typically includes a LICENSE or COPYING file.
* FSF focuses on software freedom.
* OSI focuses on open-source development and collaboration.
* Common open-source licenses include:

  * GPL
  * LGPL
  * BSD
  * MIT
  * Apache
  * Artistic
* GPL is restrictive (copyleft), while MIT and BSD are more permissive.

---


