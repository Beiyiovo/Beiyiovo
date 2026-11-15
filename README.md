### 赖振雄

从传感器驱动写到云端平台。习惯把重复劳动做成工具，也习惯把「为什么这么选」写下来——仓库里的 README 基本都是这个路子。

---

#### 我在做的三件事

**[iot-llm-platform](https://github.com/Beiyiovo/iot-llm-platform)** · `Java 21` `Spring Boot 3` `Moquette` `MySQL`
设备接入与智能诊断平台。内嵌 MQTT Broker（免装 Docker / EMQX），设备以 deviceKey + secret 一机一密接入；遥测入库 → 「连续 N 点越限」防抖告警 → 通义千问根因诊断，无 API Key 时自动降级本地规则。45 个 JUnit5 用例（核心业务类行覆盖 69%），本机压测 6 并发 9000 个数据点、约 4450 条/秒。

**[stm32-health-monitor](https://github.com/Beiyiovo/stm32-health-monitor)** · `C` `STM32F103` `ESP32-C3`
四参数生理监测终端（毕业设计）。6 路传感器驱动、24 个分步验证工程 0 错 0 警告；3 人实测心率 MAE 0.95 bpm、血氧 MAE 0.40%、体温最大误差 0.5 ℃。附带一次 I2C 排障的完整记录：分布电容导致上升沿拖尾，降速到 25 kHz 才稳定。

**[stm32-serial-flash](https://github.com/Beiyiovo/stm32-serial-flash)** · `C` `Win32` `ISP 协议`
串口一键烧录 + 串口监视，一根 USB-TTL 干两件事。波特率自适应握手——因为同一块板子昨天能烧的波特率今天可能就不行。

---

#### 能做什么

| | |
|---|---|
| **嵌入式** | STM32 / ESP32 驱动开发；软件模拟 I2C、单总线、UART；立创 EDA 原理图与 100×100 mm 双层板；Keil 与串口 ISP 烧录 |
| **后端** | Spring Boot 分层接口、MySQL 表设计与索引、JWT + RBAC、MQTT 接入、规则引擎与状态机 |
| **工具** | Python 串口自动化、批处理脚本、Git；把「每天手工做一遍」的事写成脚本 |

---

📮 2804627817@qq.com
