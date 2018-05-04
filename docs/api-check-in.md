# 用户签到接口

## 用户签到
```
POST /tbm/user/checkin
```
### 响应
```
status 204
```
## 用户签到信息
```
GET /tbm/user/checkin
```
### 响应
```
status 200
```
```json
{
    "check_in_status": true,// 今日签到状态
    "check_in_reward": 20,// 当天签到奖励
    "check_in_count": 3 // 连续签到天数
}
```
