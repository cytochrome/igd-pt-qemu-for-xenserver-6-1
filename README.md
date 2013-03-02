xen-device-model Package with Newer IGD Passthru for XenServer 6.1
------------------------------------------------------------

**Overview**

This package enables XenServer 6.1 to Passthru newer IGDs.
There are following changes from the original package.

  - Some functions related to Passthru are backported from
    xen-4.2-testing.
  - Including Intel newer IGD (like IvyBridge) specific
    codes.

**Packages**

  - xen-device-model (i386.rpm): binary package which has
    built on XenServer DDK. 
  - xen-device-model (src.rpm): source package.
  - pciutils-devel (i386.rpm): binary package of
    pciutils-devel built from  pciutils SRPM at Xen Cloud
    Platform 1.6 source-disc. (source-4.iso)
    (pciutils-devel is needed to build binary package of
     xen-device-model)

**Details for patch.**

  - add ppt_pci_get_dev
  - add PT_ERR macro.
  - change argument types of pt_pci_host_read/write.
  - fix codes which callis pt_pci_host_read/write.
  - add newer IGD specific codes.

**NOTE: My work is only for creating backport patches from
xen 4.2 (and built rpm). the original awesome patches for
IGD Passthru are located in Xen-devel.**

   1. [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]
   2. [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]
   3. [qemu-xen-trad: IGD passthrough: Expose	vendor specific pci cap on host bridge.]

**License**

Inherited from Xen Cloud Platform (GPL v2)


  [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00537.html
  [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00536.html
  [qemu-xen-trad: IGD passthrough: Expose	vendor specific pci cap on host bridge.]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00538.html
