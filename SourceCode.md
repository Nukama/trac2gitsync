---
layout: doc
title: SourceCode
permalink: /doc/SourceCode/
redirect_from: /wiki/SourceCode/
---

Qubes Source Code Repositories
==============================

All the Qubes code is kept in GIT repositories. We divided the project into several components, each of which has its own separate repository:

-   `core.git` -- the core Qubes infrastructure responsible for VM management, VM temaplates, fs sharing, etc.
-   `gui.git` -- GUI virtualization, both Dom0 and VM side.
-   `template-builder.git` - scripts and other files used to create Qubes templates and NetVM images.

You can browse the repositories [on line via GitWeb](http://gitweb.qubes-os.org/gitweb/). The Qubes official repositories are in the `mainstream` directory.

To clone a repository:

```
git clone git://qubes-os.org/mainstream/<repo_name>.git <repo_name>
```

e.g.:

```
git clone git://qubes-os.org/mainstream/core.git core.git
```

Currently the preferred way of contributing to the project is by sending a patch via the project's mailing list (`git format-patch`).
