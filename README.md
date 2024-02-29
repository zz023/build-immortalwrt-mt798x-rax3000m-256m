# immortalwrt-mt7981-rax3000m_nand_256m 云编译仓库

* 默认整合所有路由基础功能(`pppoe`、`ipv6`、`防火墙`等)，其他功能均会在`Release`简介处列出。
* 建议使用`Releases`内最新且标注“已测试”的固件。
* 感谢P3TERX,hanwckf,padavanonly,kenzo等大佬。
* 默认云编译cmcc_rax3000m_nand硬改256m版本
* 如果要编译原厂128M闪存的版本，请将diy-part2.sh脚本里面sed前面的添加注释符号#再编译
*   #修改闪存为256M版本
*  sed -i 's/<0x580000 0x7200000>/<0x580000 0xee00000>/g' target/linux/mediatek/files-5.4/arch/arm64/boot/dts/mediatek/mt7981-cmcc-rax3000m.dts
*   sed -i 's/116736k/240128k/g' target/linux/mediatek/image/mt7981.mk。
* 登陆IP:192.168.5.1
  密码：空
* 近期由于kenzo仓库添加了istore,导致和237仓库既有的istore的app在编译时冲突，请编译时注意在diy-part2.sh中加入命令删除某些重复的软件包。
