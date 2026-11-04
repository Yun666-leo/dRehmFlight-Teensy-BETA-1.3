# Transforming Quadcopter Flight Controller

本项目保存 Transforming Quadcopter 的 Teensy 4.0 飞控代码和接线说明。

## 目录

- `dRehmFlight_Teensy_BETA_1.3/`：当前活动固件、库源码和说明文档
- `dRehmFlight_Teensy_BETA_1.3/dRehmFlight_Teensy_BETA_1.3.ino`：主 sketch
- `dRehmFlight_Teensy_BETA_1.3/修复说明.md`：代码修改记录和硬件约束
- `dRehmFlight_Teensy_BETA_1.3/ESC_calibration_log.md`：电调校准和实测记录

## 当前配置

- 飞控：Teensy 4.0
- 飞行电调：标准 50Hz PWM，M1～M4，1000～2000µs
- 轮驱电调：标准 50Hz PWM，M5～M6，1500µs 停止中位
- 舵机：S1/S2，前舵机引脚 6，后舵机引脚 7
- 线性推杆：S1 第 3～6 排，Teensy 引脚 8～11，经 DRV8871 驱动
- 接收机：ELRS SBUS，接扩展板 `5` 焊盘（Teensy 引脚 21）

## 构建

使用 Arduino IDE 2.x + Teensyduino：

1. 打开 `dRehmFlight_Teensy_BETA_1.3/dRehmFlight_Teensy_BETA_1.3.ino`
2. 选择 Board `Teensy 4.0`
3. 选择对应的 Teensy Port
4. 编译并上传

不要在未拆桨、未断开执行机构电源的情况下进行首次上电测试。
