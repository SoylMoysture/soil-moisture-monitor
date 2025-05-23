# soil-moisture-monitor
An ESP32 based soil moisture monitoring system.

This project uses a [DF Robot ESP32-C6](https://wiki.dfrobot.com/SKU_DFR1075_FireBeetle_2_Board_ESP32_C6) board to leverage the following characteristics:
* Flexible connectivity:  Wi-Fi, BLE, Zigbee, and Thread. Allows future adaption into Home Automation platforms.
* Integrated power management.
* Deep sleep low-power draw (.036 mA on version 1.1)
* Solar charging enables longer running times without need for hooking up to power.
* Battery level detection to monitor power.

The project uses a capacitive sensor. These sensors are superio to resistive sensors due to their superior accuracy, durability, and resistance to corrosion.
![image](https://github.com/user-attachments/assets/11637db9-9b52-4329-9a7a-9b18123aeb44)

By integrating a solar charging element, the project aims to allow long-term operation without the need to recharge the system. Though this is highly dependent on the amount of sunlight available. With this in mind, some attention is paid to optimizing the power budget according to the following assumptions:
* Minimize active operation (sensor reading, wifi active, etc.) to reduce current draw
* Maximize deep sleep time where the unit is operating in lower power mode
* Adjust above parameters to balance calculated current draws to solar cell recharge capacity
* Be mindful of device aesthetics. Don't want to have a large solar panel overwhelming the space of the plant.








 
