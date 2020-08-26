### 1 原因：
由于github域名解析造成偶尔不能访问Github网站。
访问网址时先搜索hosts文件，如果有网址对应的ip则不需要dns域名解析，因此可以将网址的ip配成静态ip，减少解析过程，提高访问速度。

### 2 操作
hosts文件（位置为C:\Windows\System32\drivers\etc）最下面增加：

192.30.253.113 github.com
185.199.108.153 github.github.io
151.101.72.133 assets-cdn.github.com
151.101.185.194 github.global.ssl.fastly.net

### 3 刷新网络DNS缓存
打开dos窗口，执行：ipconfig /flushdns
现在您可以愉快的访问Github了。