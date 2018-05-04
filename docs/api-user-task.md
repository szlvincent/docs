# 任务

## 用户任务
```
GET /tbm/user/tasks
```
### 响应
```
status 200
```

```json
{
    "extras": {
        "invite_friend": {
            "title": "邀请好友",
            "desc": "邀请一名好友得100TBMark",
            "reward": 100
        },
        "invite_code": {
            "title": "填写邀请码",
            "desc": "填写邀请码获取8个TBMark",
            "reward": 100
        }
    },
    "tasks": [
        [
            {
                "id": 5,
                "type": "frequency",
                "frequency": 10,
                "trigger": "share",
                "reward": true,
                "amount": 1,
                "name": "分享快讯",
                "description": "分享快讯",
                "notification": false,
                "created_at": "2018-02-28 02:26:56",
                "updated_at": "2018-02-28 02:26:56",
                "deleted_at": null,
                "complete_at": "2018-03-02",
                "notes": [
                    {
                        "id": 60,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:04:52",
                        "updated_at": "2018-03-02 09:04:52"
                    },
                    {
                        "id": 61,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:06",
                        "updated_at": "2018-03-02 09:05:06"
                    },
                    {
                        "id": 62,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:07",
                        "updated_at": "2018-03-02 09:05:07"
                    },
                    {
                        "id": 63,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:08",
                        "updated_at": "2018-03-02 09:05:08"
                    },
                    {
                        "id": 64,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:08",
                        "updated_at": "2018-03-02 09:05:08"
                    },
                    {
                        "id": 65,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:09",
                        "updated_at": "2018-03-02 09:05:09"
                    },
                    {
                        "id": 66,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:10",
                        "updated_at": "2018-03-02 09:05:10"
                    },
                    {
                        "id": 67,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:11",
                        "updated_at": "2018-03-02 09:05:11"
                    },
                    {
                        "id": 68,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:11",
                        "updated_at": "2018-03-02 09:05:11"
                    },
                    {
                        "id": 69,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:12",
                        "updated_at": "2018-03-02 09:05:12"
                    },
                    {
                        "id": 70,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:13",
                        "updated_at": "2018-03-02 09:05:13"
                    },
                    {
                        "id": 71,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:14",
                        "updated_at": "2018-03-02 09:05:14"
                    },
                    {
                        "id": 72,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:05:14",
                        "updated_at": "2018-03-02 09:05:14"
                    },
                    {
                        "id": 73,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:11:55",
                        "updated_at": "2018-03-02 09:11:55"
                    },
                    {
                        "id": 74,
                        "task_id": 5,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:11:56",
                        "updated_at": "2018-03-02 09:11:56"
                    }
                ]
            }
        ],
        [
            {
                "id": 8,
                "type": "one-off",
                "frequency": 1,
                "trigger": "certification",
                "reward": true,
                "amount": 1,
                "name": "",
                "description": "",
                "notification": false,
                "created_at": "2018-02-28 02:26:56",
                "updated_at": "2018-02-28 02:26:56",
                "deleted_at": null,
                "complete_at": "2018-03-02 09:49:01",
                "notes": [
                    {
                        "id": 75,
                        "task_id": 8,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:49:01",
                        "updated_at": "2018-03-02 09:49:01"
                    }
                ]
            }
        ],
        [
            {
                "id": 9,
                "type": "cycle",
                "frequency": 1,
                "trigger": "invite-user",
                "reward": true,
                "amount": 1,
                "name": "",
                "description": "",
                "notification": false,
                "created_at": "2018-02-28 02:26:56",
                "updated_at": "2018-02-28 02:26:56",
                "deleted_at": null,
                "complete_at": "2018-03-02 09:54:09",
                "notes": [
                    {
                        "id": 76,
                        "task_id": 9,
                        "user_id": 2,
                        "created_at": "2018-03-02 09:54:09",
                        "updated_at": "2018-03-02 09:54:09"
                    }
                ]
            }
        ],
        [
            {
                "id": 10,
                "type": "one-off",
                "frequency": 1,
                "trigger": "invite-code",
                "reward": true,
                "amount": 1,
                "name": "",
                "description": "",
                "notification": false,
                "created_at": null,
                "updated_at": null,
                "deleted_at": null,
                "complete_at": null,
                "notes": []
            }
        ]
    ],
    "certified": 1,
    "invite_code": {
        "user_id": 7,
        "parent_user_id": 4,
        "created_at": null,
        "updated_at": null
    }
}
```
### 返回参数说明
| 名称 | 类型 | 描述 |
|:----:|:----:|------|
| id   | int  | 任务id|
| type | string | 任务类型:frequency 频率任务 每天次数,one-off 一次性任务, cycle 周期任务每天一次|
| frequency | int | 进度限制，配合type=frequency使用|
| trigger | string | share分享、certification认证|
| reward | bool | 是否奖励 1奖励0没有奖励|
| amount | init | 奖励金额|
| name | string | 任务名称|
| description | string | 任务说明|
| description | string | 任务介绍|
| complete_at | string | null未完成，存在时间完成|
| notes | string | 任务记录,当type=frequency，trigger=share 统计notes下面接口为当前任务完成的进度|
| certified | int | 0待审核 1已通过 2已驳回 3未认证 |
| invite_code | mix | null 未填写 object 已填写|

## 任务说明
```
GET /tbm/task/explain
```
### 响应
```
status 200
```
```json
{
    "explain": "任务说明" // 任务说明
}
```
