# soil-moisture-monitor
An ESP32 based soil moisture monitoring system.

This project uses a [DF Robot ESP32-C6](https://wiki.dfrobot.com/SKU_DFR1075_FireBeetle_2_Board_ESP32_C6) board to leverage its following characteristics:
* Flexible connectivity:  Wi-Fi, BLE, Zigbee, and Thread. Allows future adaptation into Home Automation platforms.
* Integrated power management.
* Deep sleep low-power draw (.036 mA on version 1.1)
* Built-in solar charging support. Enables longer running times without need to physically hookup the system to external charger.
* Battery level detection to monitor power.
![DFR1075](https://dfimg.dfrobot.com/store/cache3/data/DFR1075/DFR1075.jpg)

The project also uses a capacitive sensor. These sensors are superior to resistive sensors due to their higher accuracy, durability, and resistance to corrosion.

![image](https://github.com/user-attachments/assets/11637db9-9b52-4329-9a7a-9b18123aeb44)

By incorporating a solar charging element, the project aims to allow long-term operation without the need to hook the system up to an external charger. Though this is highly dependent on the amount of sunlight available. With this in mind, some attention is paid to optimizing the power budget of the system by facotring in the following criteria:
* Minimize active operation (sensor reading, wifi active, etc.) to reduce current draw
* Maximize deep sleep time where the unit is operating in lower power mode
* Adjust above parameters to balance overall system current draw vs. the solar cell recharge capacity
* Be mindful of device aesthetics. Don't want to have a large solar panel overwhelming the space of the plant.

Finally, the sensor, control unit, and solar cell will be housed in their own 3D-printed enclosures. This will let the user place the components in ways that don't overwhelm the aesthetics of the plant itself. 








 
