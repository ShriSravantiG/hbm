---
title: "Installation from binary"
linkTitle: "From binary"
description: "Instructions for installing HBM as a binary. Mostly meant for hackers who want to try out HBM on a variety of environments."
keywords: [ "binary", "installation", "hbm", "documentation", "linux" ]
date: "2017-01-27"
url: "/docs/hbm/install/binary/"
menu:
  docs:
    parent: "hbm_install"
    weight: 110
github_edit: "https://github.com/kassisol/hbm/edit/master/docs/installation/binary.md"
toc: true
---

## Get the HBM binary

You can download a specific version. To get the list of stable
release version numbers from GitHub, view the `kassisol/hbm`
[releases page](https://github.com/kassisol/hbm/releases).


### Get the Linux binary

To download a specific release version, use the following
URL patterns:

```
https://github.com/kassisol/hbm/releases/download/x.x.x/hbm
```


#### Install the Linux binary

After downloading, HBM requires this binary to be installed in your host's `$PATH`.
For example, to install the binary in `/usr/local/sbin`:

```bash
$ mv hbm /usr/local/sbin/
```

> If you already have HBM installed on your host, make sure you
> stop HBM before installing (`killall hbm`), and install the binary
> in the same location. You can find the location of the current installation
> with `dirname $(which hbm)`.


#### Run the HBM daemon on Linux

You can manually start the HBM server using:

```bash
# hbm server &
```

The GitHub repository provides sample of systemd service unit file you can use to control
the daemon through a process manager, such as systemd. You can find
this script in the [contrib directory](https://github.com/kassisol/hbm/tree/master/contrib/init/systemd).

For additional information about running the HBM in server mode, refer to
the [server command](../reference/commandline/server.md) in the HBM command
line reference.

## Upgrade HBM

To upgrade your manual installation of HBM on Linux, first kill the hbm
server:

```
# killall hbm
```

Then follow the [regular installation steps](#get-the-linux-binary).

## Next steps

Continue with the [Admin Guide](../admin/overview.md).
