# UNFINISHED PAGES 此项目正在编辑中

## MKS-TinyBee-for-Artillery-Hornet

Malin firmware For MKS-TinyBee Board to replace original Artillery Hornet board.

适用于云图创智大黄蜂3D打印机创客基地TinyBee主板所修改的马林固件。

After my original Artillery Ruby board inside Artillery Hornet die... That's all my bad... I Choose MKS-TinyBee to replace that dead borad. But it has a lot of problems. So I tweaked it. A Hornet with Tiny Bee inside LOL 😉

原机的主板被我短路烧了，掂量了掂量原配的价格然后选择了创客基地的这款MKS-TinyBee（话说大黄蜂和小蜜蜂还挺配？），调试过程中遇到了很多的问题...所以我修改了固件使其适用于云图创智大黄蜂。

## 【IMPORTANT 重点】 Wiring 接线
Basically, the original wires on the machine can find the corresponding interface connection, but the wiring of the fan is different. Due to the different pin positioning, the original fan red plug needs to be inserted into the black socket on the motherboard, and the original machine blue fan plug needs to be inserted into the magenta socket.

基本上原本机器上的线都找到对应的接口连接即可，不过风扇的接线有所不同。由于针脚定位不同，原机风扇红色端子需要插入主板的黑色插线座，原机蓝色风扇端子插入洋红色插线座。

I did not use the E1 extruder according to my needs, so I moved the driver IO interface of the extruder E1 (140 141 142) to support the power-off and motherboard cooling fan pwm speed regulation. See the picture for details:

我按照我的需求并未使用E1挤出机，所以将挤出机E1的IO接口140 141 142 挪做他用以支持打完关机和主板散热风扇pwm调速。

IO 140: Motherboard cooling fan pwm 主板散热风扇PWM

-=THIS PIN IS FAN'S GND PIN=- -=这里应连接风扇负极=-

IO 141: Kill_PIN (This pin connect relay module pin IN) (此接口连接继电器模块IN)

IO 142: PS_ON_PIN (nothing connected)
