# 课程模块\(course\)

---

## 获取课程列表 ✅

#### 路由：

GET`/course`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| courseNumber | 课程号 | string |  |  |
| courseIndex | 课序号 | string |  |  |
| courseName | 课程名 | string |  |  |
| start | 开始时间 | date |  |  |
| end | 结束时间 | date |  |  |
| teacherNumber | 任课教师工号 | string |  |  |
| pageNo | 页数 | interger |  |  |
| pageSize | 页面容量 | interger |  |  |

#### 响应：

```
[
    {
        // 课程信息
    },
    ...
]
```

## 获取课程详细信息 ✅

#### 路由：

GET `/course/:id`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| id | 课程id | interger | true |  |

#### 响应

```
{
    // 课程信息
}
```



