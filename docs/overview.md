---
title: "About HBM"
linktitle: "Overview"
description: "HBM"
keywords: [ "hbm", "about" ]
date: "2017-01-27"
url: "/docs/hbm/overview/"
menu:
  docs:
    parent: "hbm_use"
    weight: -85
github_edit: "https://github.com/kassisol/hbm/edit/master/docs/overview.md"
toc: true
---

**Secure, restrict Docker's capabilities**

[**HBM**](http://harbormaster.io) is a basic extendable
Docker Engine [access authorization plugin](https://docs.docker.com/engine/extend/plugins_authorization/)
that runs directly on the Docker host.

## Why HBM?

By default Harbormaster plugin prevents from executing commands and certains parameters.

1. Docker commands
2. Pull images
3. Start containers with specific parameters
* `--privileged`
* `--ipc=host`
* `--net=host`
* `--pid=host`
* `--userns=host`
* `--uts=host`
* any Linux capabilities with parameter `--cap-add=[]`
* any devices added with parameter `--device=[]`
* any dns servers added with parameter `--dns`
* any ports added with parameter `--port`
* any volumes mounted with parameter `-v`
* any logging with parameters `--log-driver` and `--log-opt`
* `--sysctl`
* `--security-opt`

## About this guide

### Installation guides

The [installation section](installation/overview.md) will show you how to install HBM
on a variety of platforms.

### Admin guide

To learn about HBM in more detail and to answer questions about usage and
implementation, check out the [Admin Guide](admin/overview.md).

## Release notes

A summary of the changes in each release in the current series can now be found
on the separate [Release Notes page](https://github.com/kassisol/hbm/releases)

## Licensing

HBM is licensed under the GNU GPL 3. See
[LICENSE](https://github.com/kassisol/hbm/blob/master/LICENSE) for the full
license text.
