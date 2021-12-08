cn-ignore-list
==============

[ignore.list][1] is used by [openwrt-shadowsocks][2]

```bash
wget -qO- http://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest |
  awk -F '|' '$2=="CN" && $3=="ipv4" {printf "%s/%s\n", $4, 32-log($5)/log(2)}' > ignore.list
```

[1]: https://github.com/easypi/cn-ignore-list/releases
[2]: https://github.com/shadowsocks/openwrt-shadowsocks
