# ThingsBoard 集成服务｜筹备版

**编号：** TB-001～TB-006  
**状态：** 候选服务，待 Demo、实际报价和平台类目验证；以下价格为人工费试运营假设，不是市场报价或合同承诺。

## 服务范围与参考价格

| 编号 | 服务 | 参考起步价 | 起步套餐交付物 |
| --- | --- | ---: | --- |
| TB-001 | ThingsBoard 部署与基础配置 | ¥399 | 单机测试环境部署、登录检查、配置记录 |
| TB-002 | ThingsBoard REST API 与业务系统对接 | ¥499 | 1 个明确 API 场景，鉴权与请求验证记录 |
| TB-003 | MQTT 设备数据上报接入 | ¥499 | 测试设备、数据上报、设备遥测验证 |
| TB-004 | Modbus / OPC UA 网关接入 | ¥799 | 1 类模拟或客户授权设备的最小采集链路 |
| TB-005 | 设备数据看板、规则引擎、告警 | ¥499 | 1 张基础看板或 1 条约定规则的演示验收 |
| TB-006 | ThingsBoard 二次开发及定制集成 | 需求报价 | 先付费评估范围，再签订功能开发范围 |

价格不含设备、服务器、云平台、第三方插件、许可与专用数据迁移服务。超过约定设备数、数据点、协议复杂度、远程现场支持或商用上线应重新报价。

## 技术交付链路

设备 / 模拟器 → ThingsBoard IoT Gateway（按需，支持 MQTT、Modbus、OPC UA 等 Connector）→ ThingsBoard 平台 → 时序数据、属性、规则链、告警和 Dashboard → REST API / 业务系统

可选路径：设备直接通过 ThingsBoard MQTT Device API 上报，或从外部 MQTT broker 经集成接入。具体按设备协议、版本、网络环境与授权范围决定。

## 商业许可核对（必须在报价前完成）

**特别注意：ThingsBoard 自 4.4 起改变了许可模式。** 官方宣布旧 CE/PE 合并为 BUSL 1.1 的 source-available 产品。ThingsBoard 4.4 的免费商业使用许可覆盖“保留 ThingsBoard 品牌、单台服务器、最多 100 台设备”的情形；超出设备规模或要替换品牌，需要商业许可。具体资格、服务器定义、SaaS 或历史 CE 迁移应核对官方协议与客户环境，不能自行推定永久免费。

- 官方许可说明：https://thingsboard.io/blog/one-thingsboard-source-available/
- 官方价格与适用条件：https://thingsboard.io/pricing/
- 官方部署与授权：https://thingsboard.io/docs/pe/installation/docker/
- IoT Gateway Connector：https://thingsboard.io/docs/iot-gateway/connectors/
- 官方 REST API：https://thingsboard.io/docs/reference/rest-api/

不得修改或规避许可检查；客户应自行取得合适的授权并确认法律/商业使用条件。旧版本许可须按确切版本另行审核。

## TB-003/004 最小实操验收（尚未执行）

1. 在隔离环境部署与许可条件匹配的 ThingsBoard，记录平台及 Gateway 版本。
2. 使用模拟 MQTT + Modbus（条件允许增加 OPC UA）设备接入，定义至少 3 个数据点的映射。
3. 验证遥测与设备状态正确、时间戳/数据质量可辨。
4. 验证断线重连、重复消息、异常值、失联标记及恢复快照。
5. 创建最小看板与告警，并记录接口/规则链的验证结果。
6. 整理可复现步骤、日志（脱敏）、风险说明与验收截图。

真实工业控制、远程写参数和生产设备下发命令，需要单独授权、现场安全审查及回滚预案，不属于基础服务。
