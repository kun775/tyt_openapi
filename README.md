# 本仓库为TYT_future智能配电服务器接口说明文档

**接口访问方式:** `POST`、`GET`

**服务器返回数据格式:** `JSON`

**测试服务器域名:** `http://pdapi.myrmit.cn`

**正式服务器域名:** `http://mpapi.taiyong.net`

**本地服务器域名:** `http://pdapi.tyt.com`(需要host映射实际服务器ip) 或者 `http://服务器ip:8080`

**参数名中的等同关系(属于同一个参数的不同命名，但不能混用)：**
项目地id：`project_id` = `pj_id` = `site_id`

设备编码：`machine_sn` = `device_sn`
集中器(TBGF1-J) = 智能网关(MB3-J2)：带子设备的数据集中设备

## 修改记录

|修改日期 | 版本 | 相关接口 | 修改说明 | 修改人|
| ---- | ---- | ---- | ---- | ---- |
|2023/06/23 | v1.0.0 | 创建项目文档 | 创建项目文档|hsk|
|2023/07/02 | v1.0.0 | machine_list <br>device_details | 新增接口|hsk|
|2023/07/02 | v1.0.0 | machine_info| 废弃接口|hsk|
|2023/07/02 | v1.0.0 | pd_room_info| 不再返回machine_list，设备列表通过machine_list接口获取|hsk|
|2023/07/04 | v1.0.0 | get_gateway_list| 新增接口 获取网关信息|hsk|
|2023/08/03 | v1.0.0 | machine_info| 新增通过网关筛选设备列表|hsk|
|2023/09/19 | v1.0.0 | get_pd_time_task| 新增通过网关名称筛选任务列表|hsk|
|2023/09/19 | v1.0.0 | add_pd_gateway| 新增接口 添加网关|hsk|
|2023/09/19 | v1.0.0 | add_pd_device| 新增接口 添加设备（组网）|hsk|
|2024/01/04 | v1.0.0 | get_alarm_list| 新增接口 获取告警列表|hsk|
|2024/06/05 | v1.0.0 | machine_list_all| 新增接口 获取所有设备列表，包含设备实时数据|hsk|
|2024/08/20 | v1.0.0 | get_alarm_list| 数据结构改版 |hsk|
|2024/08/23 | v1.0.0 | machine_list_all_lite| 新增接口 精简machine_list_all接口返回数据 |hsk|
|2025/06/18 | v1.0.1 | version| 新增接口，用于接口版本管理 |hsk|
|2025/06/18 | v1.0.1 | device_details<br>machine_list_all_lite<br>machine_list_all| 实时数据realtime_data部分数据改从缓存获取，以适应更快频率数据更新 |hsk|
|2025/07/31 | v1.0.2 | get_consumption_daily_data| 新增接口 获取日能耗数据 |hsk|
|2025/07/31 | v1.0.2 | get_consumption_monthly_data| 新增接口 获取月能耗数据 |hsk|
|2025/07/31 | v1.0.2 | get_consumption_yearly_data| 新增接口 获取年能耗数据 |hsk|
