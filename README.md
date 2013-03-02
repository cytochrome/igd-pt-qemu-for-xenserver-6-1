xen-device-model Package with Newer IGD Passthru for XCP-1.6
------------------------------------------------------------

**Overview**

 This package enables Xen Could Platform 1.6.10 (61809c)
to Passthru newer IGDs. There are following changes from
the original package.

  - Some functions related to Passthru are backported from
    xen-4.2-testing.
  - Including Intel newer IGD (like IvyBridge) specific
    codes.

**Packages**

  - xen-device-model (i686.rpm): binary package which has
    built on XenServer DDK. 
  - xen-device-model (src.rpm): source package.

**WARNING: USE AT YOUR OWN RISK**

  This package is work fine in my environment. however,
  there are still unconscious risks of what break your
  computers or environment.

**NOTE: My work is only for creating backport patches from
xen 4.2 (and built rpm). the original awesome patches for
IGD Passthru are located in Xen-devel.**

   1. [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]
   2. [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]
   3. [qemu-xen-trad: IGD passthrough: Expose vendor specific pci cap on host bridge.]

**Build**

 To build binary packages from source package, you may
need to install XenServer DDK-VM into XCP and need to 
install binary package of pciutils-devel (i686) into DDK-VM.

 To build binary package of pciutils-devel (i686), you
need to build from pciutils source package in source-disc
of Xen Cloud Platform 1.6 (source-1.iso)

**Details for inner patch.**

  - add ppt_pci_get_dev
  - add PT_ERR macro.
  - change argument types of pt_pci_host_read/write.
  - fix codes which callis pt_pci_host_read/write.
  - add newer IGD specific codes.

**License**

Inherited from Xen Cloud Platform (GPL v2)


  [qemu-xen-trad/pt_msi_disable: do not clear all MSI flags]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00537.html
  [qemu-xen-trad: Correctly expose PCH ISA bridge for IGD passthrough]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00536.html
  [qemu-xen-trad: IGD passthrough: Expose vendor specific pci cap on host bridge.]: http://lists.xen.org/archives/html/xen-devel/2013-02/msg00538.html
