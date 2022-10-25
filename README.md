# Comps2ks

Script to generate an initial Kickstart package list from comps.xml file.

## Requirements

`dnf` package manager >= 4.7.0

## Usage

To use you will need a "comps" file from an installation DVD or a yum/dnf `repodata` directory.

```console
./comps2ks cca56f3cffa18f1e52302dbfcf2f0250a94c8a37acd8347ed6317cb52c8369dc-c7-x86_64-comps.xml
@additional-devel
#flatpak
#subversion-gnome
#lz4
@anaconda-tools
#grub2-pc
#grub2-efi-ia32-modules
#shim-unsigned-ia32
#shim-unsigned-x64
#shim-ia32
#oscap-anaconda-addon
#dbxtool
#grub2-efi-ia32
#grub2-efi-x64
#grub2-efi-x64-modules
@backup-client
#bacula-client
#rear
@backup-server
...
```

Use `comps2ks --help` to view all available options.

```console
Usage: comps2ks [OPTS...] FILE

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -e EXCLUDE, --exclude=EXCLUDE
                        exclude groups
  -d, --defaults        show packages installed by default
```
