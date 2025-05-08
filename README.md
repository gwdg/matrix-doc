# Academic Cloud Matrix Documentation

**Website:** **https://docs.chat.academiccloud.de**

forked from [TU Dresden](https://github.com/matrix-tu-dresden-de/Dokumentation)

## Building

1. Clone the repository via either HTTPS or SSH
    * HTTPS `git clone --recurse-submodules https://github.com/gwdg/matrix-doc`
    * SSH `git clone --recurse-submodules git@github.com:gwdg/matrix-doc.git`
1. `cd matrix-doc`
1. Install [Hugo](https://gohugo.io/getting-started/installing)
1. Run `hugo server -p 1313`
1. Open http://localhost:1313/

## Upgrading the theme

When an upgrade for the theme is needed, we upgrade the associated Hugo module to the latest released version:

```sh
hugo mod get -u github.com/McShelby/hugo-theme-relearn
```

We can also upgrade to a specific commit ref:

```sh
hugo mod get -u github.com/McShelby/hugo-theme-relearn@0b83617ee9da5253aafcf11807b256da7d88d709
```
