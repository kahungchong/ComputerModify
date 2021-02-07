# Chrome 关闭证书验证
## 某些网站使用自己的证书而非第三发CA，导致浏览器无法继续访问。用户可以自行安装网站证书或通过浏览器设置绕过证书验证。以下介绍Chrome的方法。

1. 开启Terminal
2. 输入

        '/Applications/Google Chrome.app/Contents/MacOS/Google Chrome' --ignore-certificate-errors --allow-running-insecure-content
3. 回车，Chrome 浏览器将会打开。
4. 在地址栏输入网站，如提示不安全，且高级(advanced) tab没有出现process选项，则在页面空白位置输入：

        thisisunsafe
    输入完毕后，这个网址将会被加入信任名单

5. 完毕