𝐌𝐀𝐓𝐋𝐀𝐁 𝐒𝐢𝐦𝐮𝐥𝐢𝐧𝐤 - 𝐩𝐇 𝐃𝐞𝐭𝐞𝐜𝐭𝐢𝐨𝐧 𝐚𝐧𝐝 𝐑𝐞𝐠𝐮𝐥𝐚𝐭𝐢𝐨𝐧
This Simulink model represents a pH detection and regulation system. It measures the pH level using a pH sensor, processes the signal to determine the pH range, and controls a water pump to adjust the pH level accordingly. The system uses various blocks to handle signal processing, decision-making, and control tasks.

𝐄𝐱𝐩𝐥𝐚𝐧𝐚𝐭𝐢𝐨𝐧 𝐨𝐟 𝐊𝐞𝐲 𝐁𝐥𝐨𝐜𝐤 𝐃𝐢𝐚𝐠𝐫𝐚𝐦𝐬 

𝟏.𝐩𝐇 𝐒𝐞𝐧𝐬𝐨𝐫 𝐁𝐥𝐨𝐜𝐤: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block simulates the pH sensor that measures the pH level of the solution.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It generates a voltage output proportional to the pH level, which is then fed into the system for further processing.

𝟐.𝐕𝐨𝐥𝐭𝐚𝐠𝐞 𝐑𝐞𝐚𝐝𝐢𝐧𝐠 𝐁𝐥𝐨𝐜𝐤: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block converts the sensor output into a readable voltage signal.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It ensures the voltage signal is within a usable range for the subsequent blocks.

𝟑.𝐙𝐞𝐫𝐨 𝐂𝐨𝐧𝐬𝐭𝐚𝐧𝐭 𝐁𝐥𝐨𝐜𝐤: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block provides a reference voltage value.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It is used for calibration purposes, ensuring accurate pH readings by compensating for any offset in the sensor signal.

𝟒.𝐀𝐮𝐭𝐨 𝐑𝐚𝐧𝐠𝐞 𝐚𝐧𝐝 𝐁𝐚𝐬𝐢𝐜 𝐑𝐚𝐧𝐠𝐞 𝐑𝐞𝐚𝐝𝐢𝐧𝐠 𝐁𝐥𝐨𝐜𝐤𝐬: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: These blocks categorize the pH reading into different ranges (e.g., acidic, neutral, basic).
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: They help determine the appropriate action needed to regulate the pH by comparing the sensor voltage against predefined thresholds.

𝟓.𝐆𝐞𝐧𝐞𝐫𝐚𝐭𝐞 𝐒𝐢𝐠𝐧𝐚𝐥𝐬 𝐟𝐨𝐫 𝐀𝐮𝐭𝐨 𝐚𝐧𝐝 𝐁𝐚𝐬𝐢𝐜 𝐑𝐚𝐧𝐠𝐞 𝐁𝐥𝐨𝐜𝐤𝐬: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: These blocks generate control signals based on the pH range detected.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: They determine whether the pH is within the desired range or if adjustment is necessary.

𝟔.𝐎𝐍/𝐎𝐅𝐅 𝐂𝐨𝐧𝐭𝐫𝐨𝐥 𝐁𝐥𝐨𝐜𝐤: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block determines whether to activate the water pump.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It generates an ON/OFF signal based on the pH range readings and other control inputs.

𝟕.𝐖𝐚𝐭𝐞𝐫 𝐏𝐮𝐦𝐩 𝐂𝐨𝐧𝐭𝐫𝐨𝐥𝐥𝐞𝐫 𝐁𝐥𝐨𝐜𝐤: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block controls the operation of the water pump
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It adjusts the water pump's activity to regulate the pH level, turning it ON or OFF as needed.

𝟖.𝐓𝐢𝐦𝐞 𝐃𝐞𝐥𝐚𝐲 𝐑𝐞𝐚𝐝𝐢𝐧𝐠 𝐚𝐧𝐝 𝐓𝐢𝐦𝐞 𝐃𝐞𝐥𝐚𝐲 𝐟𝐨𝐫 𝐖𝐚𝐭𝐞𝐫 𝐏𝐮𝐦𝐩 𝐁𝐥𝐨𝐜𝐤𝐬:
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: These blocks introduce a time delay into the system.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: They ensure that the system doesn't react too quickly to changes, providing a more stable pH regulation by allowing time for the pump to adjust the pH level before making further adjustments.

𝟗.𝐀𝐧𝐚𝐥𝐨𝐠 𝐭𝐨 𝐃𝐢𝐠𝐢𝐭𝐚𝐥 𝐂𝐨𝐧𝐯𝐞𝐫𝐬𝐢𝐨𝐧 (𝐀𝐃𝐂) 𝐁𝐥𝐨𝐜𝐤𝐬: 
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: These blocks convert the analog signals from the pH sensor and control blocks into digital signals.
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: They prepare the signals for digital processing and control logic within the Simulink model.

𝟏𝟎.𝐏𝐮𝐦𝐩 𝐎𝐍 𝐨𝐫 𝐎𝐅𝐅 𝐑𝐞𝐚𝐝𝐞𝐫 𝐁𝐥𝐨𝐜𝐤:
𝐃𝐞𝐬𝐜𝐫𝐢𝐩𝐭𝐢𝐨𝐧: This block reads the current state of the pump (ON or OFF).
𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: It provides feedback to the system to ensure proper operation and allow for adjustments as necessary.

In summary, the model integrates sensor data acquisition, signal processing, range determination, control logic, and actuator control to maintain the desired pH level in a solution. Each block plays a crucial role in ensuring the system functions accurately and efficiently.

Screenshot of the pH Detection and Regulation Simulink Model:
![image](https://github.com/Xtiantzyyy/MATLAB-Simulink-pH-Detection-and-Regulation/assets/87014015/c78fef2e-d6e5-4a4f-902d-c97f1ef98b7e)

