# 授权模块\(auth\)

---

## 注册 ✅

#### 路由：

`POST /student/auth/signup`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| number | 学号 | string | true |  |
| academy | 学院 | string | true |  |
| phone | 手机号码 | string | true |  |
| email | 电子邮箱 | string | true |  |
| password | 密码 | string | true |  |
| name | 姓名 | string | true |  |

#### 响应：

```js
{
    "userId": 47,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlSWQiOjEsInVzZXJJZCI6NDcsImlhdCI6MTQ4ODQ2MzM2M30.Bi_z8aG9L9p-sv4Xmww3e6LT3_QlROIhZcnGQZ_VghI",
    "number": 2013141452239
}
```

## 



