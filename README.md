# CForge — Downloads

**English** · [Türkçe](README.tr.md)

CForge sets up everything your C course needs in a single operation: VS Code, a
C compiler, the required extensions, and a sample project ready to run. No
administrator rights needed.

**[→ Download page](https://cforge-indir.mtvrkan.com/)**

The installers are not in this repository. CForge is for the students of the
schools running the course: on the download page you type your name and **the
e-mail address your school issued you**, and **each student may download once a
week**. There is no code and no password.

The links you are given are good for 24 hours — a download that stops can be
resumed from the same link without costing you the week.

Product page: [cforge.mtvrkan.com](https://cforge.mtvrkan.com)

![CForge — a C development environment for first-year students](og-cover-en.png)

---

## Which one do I download?

| Your system | File |
| --- | --- |
| Windows 10/11 — **recommended** | `CForge-windows-offline-<version>.exe` |
| Windows, on a fast and unrestricted connection | `CForge-windows-online-<version>.exe` |
| Mac (Apple Silicon — M1, M2, M3, M4) | `CForge-macos-arm64-<version>.dmg` |
| Mac (Intel) | `CForge-macos-x64-<version>.dmg` |
| Linux (x64) | `CForge-linux-x64-<version>.tar.gz` |

**Not sure which Mac you have:**  → About This Mac → if the *Chip* line says
*Apple*, take arm64; if it says *Intel*, take x64.

**online vs offline:** the offline build carries VS Code and the compiler inside
it — a large file, but setup needs no connection. The online build is small and
downloads them while it runs. A campus network that blocks downloads is the
usual reason setup stops halfway, which is why the offline one is recommended.

## How to run it

**Windows** — run the `.exe` you downloaded; there is nothing to install.
It may take a few seconds to open the first time.
**If you see "Windows protected your PC"**, that is expected: CForge is not a
signed application, and Windows shows this for every program it does not
recognise. Click **More info** → **Run anyway**.

**macOS** — double-click the `.dmg`, then drag `CForge.app` onto the
**Applications** folder beside it. Launch it from Applications with
**right-click → Open** (macOS blocks a double-click on first launch). Do not skip the drag and run it
from Downloads: an app opened out of a quarantined folder is started from a
randomly named, read-only copy every time, and moving it to Applications is what
turns that off.

**Linux** — extract and run:

```bash
tar -xzf CForge-linux-x64-*.tar.gz
./CForge/CForge
```

## Checking what you downloaded

Every release carries `SHA256SUMS.txt` on its
[release page](https://github.com/mtvrkan/cforge-releases/releases/latest), and
the download page shows the SHA-256 of each file. If the two agree, the file
arrived intact.

```powershell
Get-FileHash CForge-windows-offline-*.exe -Algorithm SHA256
```

```bash
shasum -a 256 CForge-macos-arm64-*.dmg      # macOS
sha256sum CForge-linux-x64-*.tar.gz          # Linux
```

## When setup finishes

VS Code opens with `ilkprojem.c` ready. **F5** compiles and runs it. Setup
verifies the environment it just built by compiling and running a program in it
— so if it says it finished, it works.

Your project folder: `Documents/algoritma-1`.

## If something goes wrong

CForge produces a report that explains in plain language what happened, ready to
copy. Send it to your instructor — it tells apart an antivirus deletion, a
cancelled installer, an incomplete toolchain and a network that blocks
downloads.

Trying again is safe: CForge continues where it left off and does not reinstall
what is already there.

**If the download page says you have used this week's turn** and you have no
working installation, write to your instructor. The turn renews on its own, and
the page tells you when.

---

This repository holds the release notes, the checksums and the product page's
images. The installers live behind the download page.
