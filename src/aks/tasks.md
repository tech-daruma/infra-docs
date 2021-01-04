# AKS important maintanence tasks

---
**NOTE**

These are upcoming infra tasks to improve general stability and performance of AKS. These include, but are not limited to:
- Ephemeral OS disks
- Podidentity upgrade to (NMI) only mode and v1.7.1 +.
- Control Plane and Node Pool upgrades to 1.18.x
- Node Image upgrades & Automating node images (full vs semi)
- Thread of DISK I/O issues on AKS in general given [here](https://github.com/Azure/AKS/issues/1373)

---



## Ephemeral OS disks

This resolves many Disk I/O issues for container hosts in general.


---
**IMPORTANT**

With ephemeral OS you can deploy VM and instance images up to the size of the VM cache. In the AKS case, the default node OS disk configuration uses 128GB, which means that you need a VM size that has a cache larger than 128GB. The default Standard_DS2_v2 has a cache size of 86GB, which is not large enough. The Standard_DS3_v2 has a cache size of 172GB, which is large enough. You can also reduce the default size of the OS disk by using --node-osdisk-size. The minimum size for AKS images is 30GB.

---

1. General doc on using Ephemeral OS Disk with AKS in general is given [here](https://docs.microsoft.com/en-us/azure/aks/cluster-configuration#ephemeral-os)
2. 

