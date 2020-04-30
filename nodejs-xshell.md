#### 写运行程序步骤
***
1. touch one.js 建立文件

2. vi/vim 编写文件

3. i 进入编写模式

4. :wq 保存文件
### xshell
#### 关于复制粘贴
***
> `xshell内部复制粘贴`
   pp复制 y粘贴
> `xshell外部复制到shell内部`
  ctrl+c复制，insert+shift粘贴

#### 运行node.js文件关闭xshell也能运行
  1. node   .js &
  2. disown
  3. 查看node进程 ps -ef | grep node
