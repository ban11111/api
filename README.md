#### OutdoorInfo
| 字段 | 类型 | 是否索引 | 是否可以为空 | 默认值 | 是否自增 | 备注|
| --- | --- | --- | --- | --- | --- | --- |
| id | uint | N | Y |  | Y |  |
| created_at | Time | N | Y |  | N |  |
| updated_at | Time | N | Y |  | N |  |
| deleted_at | Time | N | Y |  | N |  |
| jinjian_id | string | N | Y |  | N | 进件id |
| current_address | string | N | Y |  | N | 居住地址 |
| work_address | string | N | Y |  | N | 工作地址 |
| walk_distance | float64 | N | Y |  | N | 走路距离 |
| walk_duration | float64 | N | Y |  | N | 走路时间 |
| drive_distance | float64 | N | Y |  | N | 驾车距离 |
| drive_duration | float64 | N | Y |  | N | 驾车时间 |
| taxi_cost | float64 | N | Y |  | N | 打车费用 |
| transit_distance | float64 | N | Y |  | N | 公交距离 |
| transit_duration | float64 | N | Y |  | N | 公交时间 |
| transit_line | float64 | N | Y |  | N | 公交方式 |

#### 保存及更新出行信息
    url: /api/v1/approval/external/:approval_type/CreateOrUpdateOutdoorInfo
    method: POST
    header:
    {
        SsoToken:"",
        ApprovalType:""
    }
    req: {
		"jinjian_id":       "进件id   # string",
		"current_address":  "居住地址 # string",
		"work_address":     "工作地址 # string",
		"walk_distance":    "走路距离 # float64",
		"walk_duration":    "走路时间 # float64",
		"drive_distance":   "驾车距离 # float64",
		"drive_duration":   "驾车时间 # float64",
		"taxi_cost":        "打车费用 # float64",
		"transit_distance": "公交距离 # float64",
		"transit_duration": "公交时间 # float64",
		"transit_line":     "公交方式 # float64"
	}
