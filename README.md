# xueke
学客
#### 测试账号

地址：192.168.1.92:7001

账号：testsusu  密码: 123456

#### 登录接口定义

1. 接口名 ：/user/login;

2. 类型 ：  'POST'

3. 描述：此接口用来进行登录

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
       msg : [ String]       //返回描述信息
       data   : token  //需存起来；通过请求头带给服务端进行验证
   }
   ```

   

#### 验证码接口

//获取验证码

1. 接口名 ：/captcha;

2. 类型 ：  'GET'

3. 描述：此接口用来获取验证码

```
    //接口返回数据：
    let res  =  '图片'    //res是img标签的src
```

#### 注册接口

1. 接口名 ：/user/register;

2. 类型 ：  'POST'

3. 描述：此接口用来进行注册

4. 入参: 

   ```
   var data = {
       username: [String],     //用户名      必填
       password: [String],    //密码        必填
       captcha：[String],      // 验证码      必填
       sex：0 || 1  0：女  1：男,
       age: number,              //年龄 10~120
       email : [String],      //邮箱       必填
       phone:[String],        //手机号     11位
   }
   ```
   
   5. 出参：  

   ```
   var res = {
       status  : [Number],     //状态   1：成功    0：失败
       msg : [ String]       //返回描述信息
       data    : []
   }
   ```
   
   
####  task接口
   
1. 接口名 ：/task/list;

2. 类型 ：  'POST'

3. 描述：此接口用来进行注册

4. 入参: 

```
{}
```

5. 出参：

```
taskId:  作业的id
taskName: 作业的名字 
pid: 作业父级的id  如果为null 那么为最高级的作业  如果不为null 则该任务在task_id 为parent_id 的做作业下挂载
updataAt: 更新时间
createdAt: 创建时间
```

