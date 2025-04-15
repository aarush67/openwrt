# Custom OpenWrt Image for Raspberry Pi 5

This is a custom-built OpenWrt image designed for the Raspberry Pi 5 (bcm2712 target) with an emphasis on broad Realtek driver support and integrated VPN solutions. It comes preconfigured with essential tools and networking packages for flexible, secure network setups.

---

## 📦 Features

- ✅ **Full Realtek Driver Support**  
  All available Realtek kernel modules are compiled in to ensure maximum compatibility with Realtek-based USB and PCIe network devices.

- ✅ **Built-in VPN Solutions**  
  - **OpenVPN** (via Tailgate integration)  
  - **WireGuard**

- ✅ **Essential Utilities**  
  - `usbutils`  
  - `usbip` support  
  - Full IPv6 support  
  - `usbip` utilities  
  - BusyBox shell environment  

- ✅ **Modern Kernel**  
  Based on **Linux 6.6** with extensive kernel options enabled for networking, VPN, USB, and file system flexibility.

---

## 🖥️ Target Board

- Raspberry Pi 5 (bcm2712)

---

## 📜 Build Configuration

This image was built using a custom `.config` file with:
- Initramfs and Ext4 filesystem images
- Optimized for `aarch64_cortex-a76`
- Kernel debug and networking namespaces enabled
- OpenWrt feeds:
  - packages
  - luci
  - routing
  - telephony

---

## 📥 Download & Flashing

**Coming Soon**  
(You can build it yourself using the provided `.config` in this repo — follow standard OpenWrt image build procedures.)

---

## 🔒 Security Features

- Package signature verification enabled  
- Kernel hardening options:
  - Stack protection
  - RELRO full
  - Fortify Source  
  - Seccomp

---

## 📄 Included Packages (Partial)

- `usbutils`
- `openvpn-openssl`
- `wireguard-tools`
- `iptables-nft`
- `kmod-usb-net-rtl8152`
- `kmod-usb-net-rtl8150`
- `kmod-rt2800-usb`
- `kmod-usb-hid`
- `dnsmasq`
- `dropbear`
- `firewall4`
- `odhcpd-ipv6only`
- `ppp`
- `ppp-mod-pppoe`
- `wpad-basic-mbedtls`

(And many more)

---

## 📚 Building This Image

```bash
git clone https://github.com/openwrt/openwrt.git
cd openwrt
# Copy this repo's .config into openwrt/.config
make defconfig
make menuconfig  # Optional: to tweak
make -j$(nproc)
