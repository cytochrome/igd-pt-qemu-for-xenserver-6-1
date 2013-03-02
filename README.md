xen-device-model.1.6.10 RPM Package for XenServer 6.1 to Passthru IGD
---------------

**Overview**

This package enables XenServer 6.1 to Passthru newer IGDs.
There are following changes from the original package.

  - Some functions related to Passthru are backported from xen-4.2-testing.
  - Including Intel newer IGD (like IvyBridge) specific codes.

**Details for patch.**

- add ppt_pci_get_dev
- add PT_ERR macro.
- change argument types of pt_pci_host_read/write.
- fix codes which callis pt_pci_host_read/write.
- add newer IGD specific codes.

**NOTE: My work is only for creating backport patches from xen 4.2 (and built rpm). the original awesome patches for IGD Passthru are located in Xen-devel.**

   1. [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]
   2. [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]
   3. [qemu-xen-trad: IGD passthrough: Expose	vendor specific pci cap on host bridge.]

  [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00537.html
  [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00536.html
  [qemu-xen-trad: IGD passthrough: Expose	vendor specific pci cap on host bridge.]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00538.html
