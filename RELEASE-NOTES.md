# 📦 Release Notes

## 🗓️ Version 1.0.0 - *Initial Release*

**Release Date:** 2025-04-15

---

## 🚀 Highlights

- ✅ Custom OpenWrt image targeting **Raspberry Pi 5 (bcm2712)**
- ✅ Full Realtek driver support for USB and PCIe network devices
- ✅ Built-in **Tailgate OpenVPN** and **WireGuard**
- ✅ Included `usbutils` for device management
- ✅ Modern **Linux 6.6** kernel with extensive network and USB support
- ✅ Ext4 root filesystem with Initramfs support
- ✅ Full IPv6 functionality out of the box

---

## 📦 Included Packages (Selected)

- `usbutils`
- `openvpn-openssl`
- `wireguard-tools`
- `iptables-nft`
- `dnsmasq`
- `dropbear`
- `firewall4`
- `odhcpd-ipv6only`
- `ppp` & `ppp-mod-pppoe`
- `wpad-basic-mbedtls`
- Realtek USB Ethernet modules:  
  - `kmod-usb-net-rtl8152`
  - `kmod-usb-net-rtl8150`
  - `kmod-rt2800-usb`

---

## 🔒 Security / Hardening Features

- Signed packages and signature verification
- Full stack protection and RELRO
- Fortify Source enabled
- Seccomp sandboxing enabled

---

## 🛠️ Build Notes

- Based on official OpenWrt sources
- Custom `.config` file included in the repo
- Compiled with `GCC 13.3.0` and `musl libc`
- Optimized for `aarch64_cortex-a76`

---

## 📖 Known Issues

- None reported at initial release.

---

## 📬 Feedback & Contributions

Please submit issues or pull requests via [GitHub Issues](https://github.com/your-repo/issues).

---

## 📄 License

This project is licensed under the terms of the GNU General Public License v2.0.  
See `LICENSE` file for full license text.

---

**Enjoy secure, Realtek-friendly OpenWrt on your Raspberry Pi 5!**
