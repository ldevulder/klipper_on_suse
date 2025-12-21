# Klipper on SUSE Linux

**!! This are still Work-In-Progress scripts !!**

Scripts and configuration files to natively install a Klipper environment on SUSE Linux.

For now it only supports SUSE Leap 16.0, Tumbleweed and Slowroll.

Tested on x86_64 and aarch64 architectures but should work on others as well.

The only drawback is that to be able to compile the firmware part of Klipper a cross-compiler might be needed, but you can also directly compile on the targeted architecture.

Tested on:
  - x86_64/aarch64 + Artillery Sidewinder X1 (slightly modified)
  - aarch64 + Creative Ender3 (highly modified)

## Prerequisites

### Klipper group and user

- Create `klipper` user/group:
```
# useradd -U -m klipper
```

### Clone/Download repository

`git` is needed to download this repository, but you can also download a ZIP file from GitHub and use it directly.

- `git-core` installation:
```
# sudo zypper in git-core
```

- As `klipper` user clone the repository:
```
# su - klipper
# git clone https://github.com/ldevulder/klipper_on_suse.git
```

## Klipper installation

When the prerequisites are OK you can install all as `klipper` user:
```
# su - klipper
# cd /home/klipper/klipper_on_suse
# ./install_klipper
```

At the end Klipper and his dependencies should now be up and running!
