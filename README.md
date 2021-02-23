# Chrootfile
`Dockerfile`s for `chroots`. Exists as a specification.

A `Chrootfile` should do the following things:
1. Create a folder called `root` in the CWD.
2. In `root`, download a rootfs, or download many binaries and configs.
3. If the download was a rootfs, extract it.
4. If the download was a rootfs, delete it.
5. Copy /etc/resolv.conf into the rootfs.
6. Wrap the `root` folder into a tarball.
7. Remove the `root` folder.

Example `Chrootfile`s are in the examples directory.

To run a `Chrootfile`, run:
```bash
`head -n 1 os.cfl | tr -d "#!"` $NAME_OF_CHROOTFILE
```
