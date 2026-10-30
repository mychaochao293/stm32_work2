# stm32_work2
#电控组第二次培训作业
- **黄品朝**
- ***学号20263005353***
-非阻塞延时用 SysTick 系统节拍，SysTick的硬件定时器，上电后 `HAL_Init()` 已经配好了，每 1ms 自动触发一次中断
- 每次进中断，HAL 库就把一个全局变量 `uwTick` 加 1
- 流水灯实现思路：led_set_index(led_index);按当前索引点灯，led_index = (led_index + 1) % 3;索引前进一步，为下一次做准备
