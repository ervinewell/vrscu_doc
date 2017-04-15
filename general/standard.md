# 规范

---

## 路由规范 {#路由规范}

在API server中，一条完整的路由将被划分如下：

`前缀prefix/版本version/角色role/模块module/行为action`

假定prefix为`api`，version为`v1`，我们账户（角色）授权（模块）中的登陆（行为）路由就为：

`api/v1/auth/login`

之后，我们的api会按照角色进行划分。

## 授权 {#授权}

### 私钥访问 {#公钥访问}

用户登录成功后，将会获得他自己的私钥`token`，作为访问其对应角色的`api`的身份认证；此时，你需要在HTTP Header中传递`Authorization`头部，并附上私钥：

```
Authorization: Bearer xxx私钥
```

现在，一个完整请求头应当是\(非文件上传请求\)：

```
Content-Type: application/json
Accept: application/json
Authorization: Bearer xxxx密钥
```

## 分页 {#分页}

通常，获得列表的地方需要传递两个参数：

* `pageSize`: 页面容量
* `pageNo`： 当前页，默认从0开始

若想获取所有内容，则**不传**这两个参数。

