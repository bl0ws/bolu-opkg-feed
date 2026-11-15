# bolu-opkg-feed

Opkg feed untuk firmware BoluWrt (Bolt BL100/BL201).

Paket .ipk + index `Packages` dari release v4.3 repo `yhpgi/openwrt-bl201-boluwrt` (kernel 5.15.113).

## Pakai di router

Tambah feed di `/etc/opkg/customfeeds.conf`:

```
src/gz bolu https://cdn.jsdelivr.net/gh/bl0ws/bolu-opkg-feed@main/packages
```

Lalu:

```
opkg update
opkg install <nama-paket>
```

Catatan: paket `kmod-*` hanya bisa dipasang kalau kernel router sama persis (5.15.113). BoluWrt v6 (kernel 5.4.188) sudah punya WireGuard bawaan, jadi tidak perlu install kmod dari feed ini.
