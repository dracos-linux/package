```bash
CARA MENGHASILKAN RELEASE
hasilkan paket
di /home/me/dracos
apt-ftparchive generate -c=aptftp.conf aptgenerate.conf

file Release di dracos/dists/dracos
apt-ftparchive release -c=aptftp.conf dists/dracos >dists/dracos/Release


gpg -u B46F614C1FB353FE -bao dists/dracos/Release.gpg dists/dracos/Release

gpg -u B46F614C1FB353FE --clear-sign --output dists/dracos/InRelease dists/dracos/Release

Setiap kali Anda membuat perubahan pada repositori, Anda perlu menjalankan langkah 3 hingga 6 lagi.
```
