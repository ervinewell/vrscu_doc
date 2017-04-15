# 课程模块\(course\)

---

## 添加课程 ✅

#### 路由：

`PUT /teacher/course`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| courseNumber | 课程号 | string | true |  |
| courseIndex | 课序号 | string | true |  |
| name | 课程名 | string | true |  |
| teacherIds | 教师ID | array | true | 一门课可能有多个教师上课 |
| assistantIds | 助教ID | array |  | 一门课可能没有/有多个助教协同 |
| start | 课程起始时间 | date | true | YYYY-MM-DD |
| end | 课程结束时间 | date | true | YYYY-MM-DD |

#### 响应

```
{
    // 课程信息
}
```

## 获取课程列表 ✅

#### 路由

`GET /teacher/course`

#### 参数：

| 参数 | 描述 | 类型 | 必填 | 备注 |
| :--- | :--- | :--- | :--- | :--- |
| pageNo | 页数 | int |  |  |
| pageSize | 页面容量 | int |  |  |

#### 响应

```
[
    {
        // 课程信息
    },
    ...
]
```





