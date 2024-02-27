# immortalwrt-mt7981-rax3000m_nand 云编译仓库

* 默认整合所有路由基础功能(`pppoe`、`ipv6`、`防火墙`等)，其他功能均会在`Release`简介处列出。
* 建议使用`Releases`内最新且标注“已测试”的固件。
* 感谢hanwckf,padavanonly,kenzo等大佬。
* 默认云编译cmcc_rax3000m_nand原厂版本（128M闪存）
* 如果要编译硬改256M闪存的版本，请将diy-part2.sh脚本里面sed前面的注释符号#删除后再编译
   #修改闪存为256M版本
   #sed -i 's/<0x580000 0x7200000>/<0x580000 0xee00000>/g' target/linux/mediatek/files-5.4/arch/arm64/boot/dts/mediatek/mt7981-cmcc-rax3000m.dts
   #sed -i 's/116736k/240128k/g' target/linux/mediatek/image/mt7981.mk。
* 登陆IP:192.168.5.1
  密码：空
