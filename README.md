# xueke
学客
#### 测试账号

地址：192.168.1.92:7001

账号：testsusu  密码: 123456

#### 登录接口定义

1. 接口名 ：/user/login;

2. 类型 ：  'POST'

3. 描述：此接口用来进行cms登录

4. 入参: 

   ```
   var data = {
       username: [String],     //用户名
       password: [String],    //密码
       captcha：[String]
   }
   ```

5. 出参：  

   ```
   var res = {
       status  : [Number],     //状态   1：成功    0：失败
       message : [ String]       //返回描述信息
       data    : [String  token]  //需存起来；通过请求头带给服务端进行验证
   }
   ```

   

#### 验证码接口

//获取验证码

    let interface =  "/captcha"
    let type = 'GET';
    let params = {};
    //接口返回数据：
    let res  =  '图片'    //res是img标签的src

