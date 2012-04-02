---
layout: doc
title: AssigningDevices
permalink: /doc/AssigningDevices/
redirect_from: /wiki/AssigningDevices/
---

In order to assign a whole PCI/e device to a VM one should use ```qvm-pci``` tool. E.g.

```
lspci
```

Find the BDF address of the device you want to assign, and then:

```
qvm-pci -a <vmname> <bdf>
```

E.g. assuming 00:1a.0 is a BDF of the device I want to assign to "personal" domain:

```
qvm-pci -a personal 00:1a.0
```

Note that one can only assign full PCI or PCI Express devices. This means one cannot assign single USB devices -- only the whole USB controller with whatever USB devices connected to it. This limit is imposed by PC and VT-d architecture.