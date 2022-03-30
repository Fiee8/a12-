# a12-由 jelbrekLib64e 提供支持
支持的
A12 设备
未来支持
所有 A7-A11 设备
使用说明
目前，它将在 trustcache 中获取 root、unsandbox 和注入二进制文件。但是，jailrbeakd 不工作，并且运行二进制文件（即 dropbear 和 uicache）并且不工作

凭证交换用于 16K 设备
二进制文件位于：/var/containers/Bundle/iosbinpack64
启动守护进程位于 /var/containers/Bundle/iosbinpack64/LaunchDaemons
/var/containers/Bundle/tweaksupport 包含一个文件系统模拟，其中安装了调整和东西
符号链接包括：/var/LIB、/var/ulb、/var/bin、/var/sbin、/var/Apps、/var/libexec
所有可执行文件必须至少具有以下两个权利：

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>platform-application</key>
    <true/>
    <key>com.apple.private.security.container-required</key>
    <false/>
</dict>
</plist>
调整和其他东西安装在：/var/containers/Bundle/tweaksupport 中，就像你对 Electra beta 所做的那样。
必须使用提供的修补程序脚本修补调整。（仅限 Mac/Linux/iOS）或使用十六进制编辑器手动
应用程序安装在 /var/Apps 中，稍后您需要运行 /var/containers/Bundle/iosbinpack64/usr/bin/uicache （其他 uicache 二进制文件不起作用）
iOS 12
amfid 已修补，但它要求您使用证书辞职。像往常一样使用codesign -s 'IDENTITY' --entitlements /path/to/entitlements.xml --force /path/to/binary 或注入所有东西。但是请注意，很快我将不再在越狱时自动注入东西！
您可以调整 App Store 应用程序，但您必须自己调用越狱的 fixMmap()或使用真正的证书辞职，amfid 会为您处理。首选第二个选项。有关如何操作，请参阅上一点。
这并不危险，也不会把你搞砸。
为 rootlessJB 1.0 和 2.0 预先修补的调整将不起作用。使用新的修补程序脚本。（ldid 被替换为 ldid2！）
修补程序用法：./patcher /path/to/deb /path/to/output_folder

TODO（iOS 12-12.1.2、A12 设备）
创建 pmap 绕过以启用二进制文件的可执行映射
使用 trustcache 修复补丁查找器
测试测试测试
感谢：Ian Beer、Brandon Azad、Jonathan Levin、Electra 团队、IBSparkes、Sammy Guichelaar、Sam Bingner、xSpiral 团队



Chr1s
chr1s0x1
