# 授权模块\(auth\)

## 教师注册

#### 路由：

`/teacher/auth/signup`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| phone | 手机号码 | string | true |  |
| email | 电子邮箱 | string | true |  |
| password | 密码 | string | true |  |
| type | 教师类型 | int | true | 1-教师 2-助教 |
| name | 姓名 | string | true |  |

#### 请求示例

```js
{
    "type": 1,
    "phone": "18380140713",
    "password": "1234",
    "email": "bohesody@qq.com",
    "name": "魏如松"
}
```

#### 响应

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

## 学生注册

#### 路由

\`/student/auth/signup\`



