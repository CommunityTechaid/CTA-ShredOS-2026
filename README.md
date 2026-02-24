# CTA ShredOS 2026

Rather than try and merge the changes from upstream in the ShredOS fork, the idea is to take what works and build it using the latest Buildroot release.

## Steps

- Grab Buildroot
- Dump any superfluous `./boards/` and `./configs` for clarity
- Copy `./board/shredos/*` and `./configs/shredos_defconfig`
- Copy `./package/kernel_cmdline_extractor`
- Add `kernel_cmdline_extractor` to package config
- Edit configs to remove depricated options (eg., directfb and libhid)
- Build
- Proceed as normal.

## ToDo
- Check kernel config in `./boards/shredos` for legacy options 
- Test removing ext2 root fs as only `bzImage` is used to generate .img
- Test removing tar root fs as only `bzImage` is used to generate .img
- Diff upstream's shredos_defconfig & kernel configs against ours to check differences are sane.
