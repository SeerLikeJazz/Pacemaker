# Pacemaker

>## 外观
![](/Image/Top.jpg)  

![](/Image/Bot.jpg)

>## 使用说明
- ### 安卓手机安装nRF connect
![](/Image/app.jpg)
- ### 搜索到“Pacemaker-V1”设备，并点击“CONNECT”   
![](/Image/search.jpg)  
- ### 1.点击三点符号；2.使能CCCDs   
![](/Image/CCCD.jpg) 
- ### 发送指令   
![](/Image/RX.jpg) 
- ### 参数设置格式：IWFT   
#### I(电流)->   
输入参数：1，2，3，4，5  
对应关系：1=100uA，2=200uA, 3=300uA, 4=400uA, 5=500uA  
#### W(脉宽)->      
输入参数：1，2，3，4  
对应关系：1=1ms，2=2ms，3=3ms，4=4ms  
#### F(频率)->   
输入参数：1，2，3，4  
对应关系：1=2000ms，2=1000ms，3=500ms，4=333ms  
#### 默认输出为：300uA，2ms，1000ms
>## 示例

* 1 手机发送：123T         
![](/Image/123T.jpg)   

* 1 对应示波器显示       
![](/Image/tek123T.bmp)

* 2 手机发送：242T        
![](/Image/242T.jpg)  

* 2 对应示波器显示      
![](/Image/tek242T.bmp)  

>## 更新说明
### 22.06.09
- 编写使用说明
- 示波器校准了3个输入参数
- 调整Howland参数

### 22.06.04
- 抽象出I、W、F 3三个参数（电流，脉宽，频率）
- 'xxxT'指令格式，nRF connect带设置成功回显
- 到公司需使用示波器，校准I、W参数

### 22.06.03
BLE的RXTX和开发板的连接方式需要交换  
- 频率F：0.5-3Hz. 2000ms，1000ms，500ms，333ms
- 电流I：100-500uA. 100uA, 200uA, 300uA, 400uA, 500uA
- 脉宽W：1-4ms. 1ms, 2ms, 3ms, 4ms

- DAC输出，电流最大Io=Vin/R10=400uA，模拟负载500欧姆
- CPC4051 LDO1输出3.3V，给刺激器供电
