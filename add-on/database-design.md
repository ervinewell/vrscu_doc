# 数据库设计

---

> 所有表都有`createdAt`,`updatedAt`字段，不再赘述。

## 用户表-user

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| phone | 电话号码 | string | true |  |  | 唯一 |  |
| password | 密码 | string | true |  |  |  |  |
| roleId | 角色 | int | true |  |  | foreign\(Role\) |  |
| actived | 是否有效 | boolean | true | true |  |  |  |

## 教师表-teacher

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| roleId | 教师类型 | int | true |  |  |  | 教师/助教 |
| name | 姓名 | string | true |  |  |  |  |
| phone | 电话 | string | true |  | 唯一 |  |  |
| email | 邮箱地址 | string | true |  | 唯一 |  |  |
| userId | 用户ID | int | true |  | 唯一 | foreign\(User\) |  |

## 学生表-student

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| name | 姓名 | string | true |  |  |  |  |
| number | 学号 | string | true |  | 唯一 |  |  |
| phone | 电话 | string | true |  | 唯一 |  |  |
| email | 邮箱地址 | string | true |  | 唯一 |  |  |
| grade | 年级 | int | true |  |  |  |  |
| academy | 学院 | string | true |  |  |  |  |
| userId | 用户ID | int | true |  | 唯一 | foreign\(User\) |  |

## 课程表-course

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  |  | primary |  |
| number | 课程号 | string | true |  |  |  |  |
| index | 课序号 | string | true |  |  |  |  |
| name | 课程名 | string | true |  |  |  |  |
| creatorId | 创建者ID | int | true |  |  |  |  |

## 教师-课程中间表-teacher\_\_course

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| courseId | 课程ID | int | true |  |  | foreign\(Course\) |  |
| teacherId | 教师ID | int | true |  |  | foreign\(Teacher\) |  |

## 学生-课程中间表-student\_\_course

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| studentId | 选课学生Id | int | true |  |  | foreign\(Student\) |  |
| courseId | 课程ID | int | true |  |  | foreign\(Course\) |  |
| isCanceled | 是否退课 | bool | true | 0 |  |  |  |

## 课堂活动表-activity

| 名称 | 描述 | 类型 | 非空 | 默认 | 限定 | 键类型 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| id | 索引 | int | true |  | 自增 | primary |  |
| name | 名称 | string | true |  |  |  |  |
| type | 活动类型 | int | true |  |  |  | 详见“术语映射” |
| courseId | 所属课程ID | int | true |  |  |  |  |

## 演讲表-speech

## 演讲记录表-speechRecord

## 作业表-homework

## 作业记录表-homeworkRecord



