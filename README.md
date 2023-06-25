# MyHexoBlog
我本地的hexo博客文件夹，用于机器间转移,安装好nodejs之后，在目录执行npm install。

安装 Hexo
所有必备的应用程序安装完成后，即可使用 npm 安装 Hexo。

$ npm install -g hexo-cli
进阶安装和使用
对于熟悉 npm 的进阶用户，可以仅局部安装 hexo 包。

$ npm install hexo
安装以后，可以使用以下两种方式执行 Hexo：

npx hexo <command>
Linux 用户可以将 Hexo 所在的目录下的 node_modules 添加到环境变量之中即可直接使用 hexo <command>：
echo 'PATH="$PATH:./node_modules/.bin"' >> ~/.profile

官方文档：
https://hexo.io/zh-cn/
