# CUTSAPAY VPN

Autoinstall SSH, Xray dan UDP untuk VPS dengan izin IP GitHub.

## OS yang Didukung

- Ubuntu 20.04, 22.04, 24.04, 26.04 dan 26.10.
- Debian 12 dan 13.
- Arsitektur amd64/x86_64 dengan systemd.

## Persiapan Sebelum Install

- Gunakan VPS baru/bersih.
- Login SSH sebagai root.
- Daftarkan IPv4 publik VPS pada [daftar izin IP](https://github.com/jmsstore/permission/blob/main/izin-ip).
- Siapkan domain/subdomain dan email untuk SSL.
- Arahkan DNS A domain ke IP VPS.
- Jika memakai Cloudflare, gunakan DNS only.
- Pastikan port TCP 80 dan 443 terbuka.

## Perintah Instalasi

Salin seluruh perintah berikut ke terminal VPS:

```bash
apt-get update && apt-get install -y curl ca-certificates &&
curl -4 -fsSL https://raw.githubusercontent.com/jmsstore/cutsapay/main/setup.sh -o /root/cutsapay-setup.sh &&
chmod +x /root/cutsapay-setup.sh &&
/root/cutsapay-setup.sh
```

Installer berbentuk binary Linux. Jalankan langsung seperti di atas.

Setelah instalasi berhasil, file installer dihapus otomatis. Jika gagal, installer dan source pemeriksaan tetap disimpan.

Untuk membuka menu:

```bash
menu
```

Pembaruan tersedia melalui menu **11 Update Script**.
