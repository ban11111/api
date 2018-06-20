#### OutdoorInfo
| 字段 | 类型 | 是否索引 | 是否可以为空 | 默认值 | 是否自增 | 备注|
| --- | --- | --- | --- | --- | --- | --- |
| id | uint | N | Y |  | Y |  |
| created_at | Time | N | Y |  | N |  |
| updated_at | Time | N | Y |  | N |  |
| deleted_at | Time | N | Y |  | N |  |
| jinjian_id | string | N | Y |  | N |  |
| current_address | string | N | Y |  | N |  |
| work_address | string | N | Y |  | N |  |
| walk_distance | float64 | N | Y |  | N |  |
| walk_duration | float64 | N | Y |  | N |  |
| drive_distance | float64 | N | Y |  | N |  |
| drive_duration | float64 | N | Y |  | N |  |
| taxi_cost | float64 | N | Y |  | N |  |
| transit_distance | float64 | N | Y |  | N |  |
| transit_duration | float64 | N | Y |  | N |  |
| transit_line | float64 | N | Y |  | N |  |

#### 保存及更新出行信息
    url: /api/v1/approval/external/:approval_type/CreateOrUpdateOutdoorInfo
    method: POST
    header:
    {
        SsoToken:"",
        ApprovalType:""
    }
    req: {
		"jinjian_id":       " # string",
		"current_address":  " # string",
		"work_address":     " # string",
		"walk_distance":    " # float64",
		"walk_duration":    " # float64",
		"drive_distance":   " # float64",
		"drive_duration":   " # float64",
		"taxi_cost":        " # float64",
		"transit_distance": " # float64",
		"transit_duration": " # float64",
		"transit_line":     " # float64"
	}
