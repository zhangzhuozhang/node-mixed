## express框架
* 项目框架建立 <span style="color:red">在已经安装了node.js基础上</span>
> 1. `express myfirstexpress # express -e`       myfirstexpress表示文件名
> 2. `npm init`  安装package.json依赖
> 3. `npm i express --save/npm i express -S`  安装插件
> 4. `DEBUG=03-quick-start:* npm start` 执行项目
> 5. 在浏览器中输入网址 [app](http://127.0.0.1:3000/)
***
* 关于跨域问题
> 1. 在新建的express项目中npm install --save cros
>
> 2. 在app.js中添加var cors=require("cors"); app.use(cors());
>
> 3. 在bin/www中修改端口号
>     var port = normalizePort(process.env.PORT || '3003');
>     app.set('port',port);
***
##  react 和 express 前后端传值问题
`get请求`
* react前端：
```(javascript)
    fetch('http://47.98.163.228:3003/insertSex/'+this.props.match.params.id)
    .then(res=>res.json())
    .then(res=>{
      console.log('男女：',res);
    })
```
* express后端
```(javascript)
router.get('/insertSex/:id',function(req,res){
  var userid=req.params.id
  con.query(`select userSex from users where userId=${userid}`,function(err,result){   
      // console.log(JSON.stringify(result))
      // console.log(result[0].userSex)
      res.json(result[0].userSex)
})
})
```