---
layout: doc
title: StickMounting
permalink: /doc/StickMounting/
redirect_from: /wiki/StickMounting/
---

This requires qubes-core-appvm-1.0.1 of higher.

1.  Insert your USB stick.

1.  In Dom0 konsole (running as normal user) do:

```
xm block-attach <vmname> phy:/dev/sdb1 /dev/xvdi w
```

This assumes that your stick is seen by Dom0 kernel as **/dev/sdb** and you're mounting its first partition, so **/dev/sdb1** (the usual case).

1.  Open Dolphin file manager in the AppVM. Your stick should be visible in the "Places" panel on the left. Just click on the device.

1.  When you finish using your USB stick, right-click its icon in Dolphin and chose "Safely Remove \<Your stick name\>".

1.  Back to Dom0 konsole -- in order to unmount the stick do the following:

```
xm block-detach random /dev/xvdi
```

1.  You can remove the device.

Needless to say, we will be adding support for USB mounting to our GUI Qubes Manager so that the user will not need to use console in Dom0 -- just click a button. Coming soon, stay tuned!