# Converting-OVA-to-qcow-in-MAC-M1
Converting an OVA file into qcow2 file in MAC M1 (Apple Silicon)

## OVA
An OVA file, or Open Virtual Appliance (also sometimes referred to as Open Virtual Application), is a package that contains various files necessary to run a virtual machine. This package is a single archive file with the .ova extension and typically includes a VM's configuration file (usually in XML format), one or more virtual disks, and sometimes a manifest and certificate files.

## qcow2
qcow2 is a file format for disk image files used by QEMU, a free and open-source emulator and virtualizer. The acronym qcow stands for "QEMU Copy On Write,"
The qcow2 format is particularly useful for virtual environments where disk space efficiency and the ability to quickly revert to a known configuration are important.

## Installing home brew

```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"````

## Installing qemu utils

brew install qemu```

brew install qemu-utils```

## Check for successful instillation 

qemu-system-x86_64 --version```

## Extracting the OVA file

tar -xvf file_name.ova```

You will get two file, file_name.ovf and file_name.vmdk

## Now convert the file_name.vmdk into a .qcow using the following command

qemu-img convert -0 qcow2 file_name-disk1.vmdk file_name.qcow2```
