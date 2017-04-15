# 课程模块\(course\)

---

## 绑定课程 ✅

#### 路由：

`PUT /student/course`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| courseId | 课程ID | int | true |  |

#### 响应：

```
{

}
```

## 获取课程列表 ✅

#### 路由：

`GET /student/course`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| pageNo | 页数 | int |  |  |
| pageSize | 页面容量 | int |  |  |

#### 响应：

```
[
    {
        // 课程信息
    },
    ...
]
```


