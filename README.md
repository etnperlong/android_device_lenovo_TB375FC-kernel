# TB375FC prebuilt kernel - DerpFest 17

Prebuilt kernel for the Lenovo Xiaoxin Pad Pro 12.7 (2025), `TB375FC`
(MediaTek Dimensity 8300 / MT6897), as used by the DerpFest 17 (Android 17)
device tree.

## Contents

| Path | Description |
|------|-------------|
| `Image.gz` | gzip-compressed arm64 kernel image |
| `modules/` | kernel modules (`.ko`) plus the `system_dlkm` / `vendor_dlkm` / `vendor_ramdisk` load-order lists |
| `kernel-uapi-headers.tar.gz` | exported UAPI headers |

## Image

```
Linux version 6.1.173-android14-11-g2cb2e678e9eb
Android clang 17.0.2 (r487747c), LLD 17.0.2
```

6.1 GKI kernel on the `android14-11` KMI. MT6897 device-specific drivers that
have no published source ship as stock `.ko`; KMI stability lets them load
against this Image. These describe the checked-in reference prebuilts and do
not indicate that the DerpFest device-tree prebuilts have changed.

This checkout contains reference prebuilts only. The DerpFest device tree
consumes its own kernel, DTB and modules from
`device/lenovo/TB375FC/prebuilts/` via `TARGET_PREBUILT_KERNEL`.
