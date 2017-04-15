# 授权模块\(auth\)

---

## 登录 ✅

#### 路由：

`POST /user/auth/login`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| phone | 手机号码 | string | true |  |
| password | 密码 | string | true |  |

#### 响应：

```js
{
    "userId": 47,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlSWQiOjEsInVzZXJJZCI6NDcsImlhdCI6MTQ4ODQ2MzM2M30.Bi_z8aG9L9p-sv4Xmww3e6LT3_QlROIhZcnGQZ_VghI",
    "roleId": 1,
    "name": "魏如松",
    "email": "bohesody@qq.com",
    "type": 1
}
```

## 



