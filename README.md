# Water-Level-Detector
As part of the course module EN1190 Engineering Design Project, we were given to make a project and demonstrate that. We have started this project in the beginning of the semester 02. We planned to make a water level sensor to get alert about the water level in tanks to avoid the problems due to the water.After that we have worked together throughout that entire semester and now we have finished that completely. Now our project is ready to demonstration. We selected to use Atmega328P micro controller. Then we analyzed the all feasibilities and all possibilities. The Design of PCB and Enclosure was done using Altium software and Solid works software respectively. This report is written in order to explain the functionality, how we approach and implement to achieve the desired task, important issues faced during the project progress and the solution we came up.

## Introduction
* In some households, there are water tanks located in their backyards, which can be quite far from the main house. This distance makes it challenging to hear when the tank is overflowing from inside the house. As a result, when they turn on the water pump, they must go closer to the tank and wait until they hear the sound of water overflowing. Only then can they rush to switch off the pump.

* Imagine if they could monitor the water tank’s status from inside the house. This would allow them to easily control the water pump without the need to go outside. Additionally, in cases where they are occupied with work or other activities, receiving notifications about the water level would enable them to turn off the pump at the right time and prevent overflow.

* In areas prone to power outages, it can be a significant problem if the water tank is empty. Without power and water, it can be extremely inconvenient to stay in the house. Consider the convenience of being able to check the water level in the tank and knowing the schedule for power cuts. With this information, they could make informed decisions about whether the remaining water will suffice during the power outage or if it’s necessary to refill the tank just before the power is cut.

* Furthermore, in scenarios where a person lives alone and the water tank runs empty while they are in the bathroom or toilet, it can be uncomfortable for them to come out and switch on the water pump manually. What if they could receive an alert when the water level drops below a certain threshold (e.g., 15% of the full tank or a customizable level)? They could then remotely activate the water pump, eliminating the inconvenience.

* At night, when someone is watching TV, working, or playing mobile games and they forget to turn off the water pump, the pump may continue running unnecessarily. This leads to water and power wastage, potential damage to the pump, and the risk of the well’s water level dropping below the pump’s inlet pipe. Receiving an alert to switch off the pump would help them avoid these issues.

In summary, having a system that provides real-time information about the water tank’s status, power cut schedules, and the ability to remotely control the water pump can greatly improve convenience, prevent wastage, and ensure a continuous water supply in various scenarios.

## Problem Validation
We have conducted a comprehensive survey using Google Forms to gather quantitative feedback and gain insights into the expectations of potential end-users. The goal was to validate the identified problem statement and assess the level of demand for our proposed solution.
Survey Link: Survey Results

According to the survey findings, an impressive 76.2% of respondents reported that they have experienced the need to manually switch off their water pump immediately after their tank is filled to capacity. Additionally, a significant number of respondents admitted to frequently forgetting to turn off the pump, leading to overflow issues.
Furthermore, it was found that a rare but notable occurrence was the depletion of the water tank during power outages. Among those who faced this issue, a remarkable 91.7% expressed a desire for several key features:
* Real-time Tank Water Level Monitoring: They wish to have a system that provides continuous updates on the water tank’s water level.
* Synchronization with Power Cut Schedules: Respondents expressed interest in aligning their water tank refilling activities with scheduled power cut periods to ensure uninterrupted water supply during these times.
* Low Water Level Alerts: An overwhelming majority indicated their preference for receiving alerts just before the water level reaches a critically low point or when the tank is on the verge of overflowing.
* Moreover, approximately two-thirds of the respondents indicated a preference for a battery-operated system to power this solution.


## Solution
We propose a solution to effectively address these concerns. Our plan involves designing a system capable of monitoring the water level in the tank and providing continuous notifications to the user 24/7. This device will be securely fixed on top of the water tank and will incorporate an ultrasound wave generator and receiver.
Here’s how our system works:
* Ultrasound Measurement: The system initiates by sending an ultrasound wave through the device, which then travels down into the water inside the tank.
* Reflection and Sensing: The ultrasound waves will bounce off the water’s surface within the tank and return to the device, where they are detected by specialized sensors.
* Time Difference Calculation: The device utilizes an integrated circuit (IC) to precisely measure the time it takes for the ultrasound waves to travel from the device to the water’s surface and back.
* Calculating Empty Space: By multiplying half of the time difference by the speed of ultrasound waves, we can accurately calculate the height of the empty space within the water tank.
* Percentage Calculation: We already know the total height of the tank. With this information, we can calculate the percentage of water in the tank using the formula:
* Percentage of water in the tank = (Height of the tank – Height of empty space in the water tank) / (Height of the water tank) × 100%
* User Notifications: Based on the calculated percentage of water in the tank, our system will send timely notifications to the user. For instance, if the water level falls below a user-defined threshold (e.g., 15%), the user will receive an alert.
* Overflow Prevention: If the water level is approaching full capacity (e.g., over 95%), the user will be alerted in advance. This enables the user to take action and switch off the water pump to prevent overflow, eliminating the need to strain to hear the sound of water overflowing from the tank.
Additionally, we recommend considering the possibility of returning the overflow water to the well to reduce water wastage. However, it’s essential to note that our system primarily addresses the issues related to water level monitoring and notification. While we can’t prevent power wastage, we can help users avoid motor coil damage and ensure a more efficient water supply management.By implementing this system, users can enjoy peace of mind, knowing that they will be promptly informed about their water tank’s status and can take appropriate actions to prevent issues such as overflow or running out of water during power cuts.


## Technical Specifications
Our product is designed with a focus on technical feasibility, low power consumption, and ease of use. Here are the technical specifications for our device:

### General Specifications:

* Power Supply: 5 to 12 V DC (Rechargeable)
* Weight: 400 g – 600 g
* Bluetooth Signal Range: 100 meters
* Manual Control: Yes
* Energy Storage: Rechargeable Battery
* No Threats, No Pollution
  
## Component Details:
* Atmega 328P Microcontroller: Weight: 2.16 g, Power Consumption: 100 mW
* Ultrasonic Sensor HC-SR04: Weight: 8.5 g, Power Consumption: 75 mW
* Bluetooth Module HC-06: Weight: 4 g, Power Consumption: 240 mW
* 16 MHz Oscillator: Weight: 0.53 g, Power Consumption: 60 mW
* PCB: Weight: 22 g, Power Consumption: 100 mW
* Enclosure: Weight: 410 g
Other Components: Weight: 21 g, Power Consumption: 120 mW
*Technical Accuracy (Power & Weight):
* Total Weight of Components: 468.19 g
* Total Power Consumption: 695 mW
  
### Budget:
Total Estimated Cost: 7752 LKR

Note: The power consumption values are approximate and represent the maximum power usage of each component in the device. The actual power consumption may vary depending on usage and operating conditions.

## UI Design
Link for mobile app download :- https://bit.ly/3T5Wd2W

## PCB Design
![image](https://github.com/malanban/Water-Level-Detector/assets/131769448/653e92af-0ca4-4ddc-ae53-f8bfe1b93b7e)
![image](https://github.com/malanban/Water-Level-Detector/assets/131769448/51183332-7342-4e12-a456-802412e7ccbe)


## Enclosure Design
![image](https://github.com/malanban/Water-Level-Detector/assets/131769448/f33f0dc7-e3fb-4ced-ba70-5ebca97d06e1)


## Discussion
Throughout the execution of this project, we encountered several noteworthy challenges and obstacles, which we successfully addressed. Here are some of the key challenges we faced:

* Complex Device Design: One of the primary challenges we encountered was the complexity of designing our device. This complexity arose from the need to securely mount the ultrasonic sensor within the device, along with accommodating a rechargeable battery and charging port. We had to meticulously calculate the size of holes and ports, as well as determine the overall dimensions of the enclosure.
* Signal Reflection: Initially, we faced uncertainties regarding the reflection of signals on the surface of the water. We needed to ensure that the ultrasonic sensor could effectively send and receive signals in this environment. After careful consideration, we selected the ultrasonic sensor as the most suitable sensor for our device.
* Data Transfer: Another challenge we encountered was transferring data from the tank to a mobile device. We initially had concerns about the limited range of Bluetooth modules, which were reported to have a range of only 10 meters. However, we eventually identified a Bluetooth module that could transmit data within a 100-meter radius, overcoming this limitation.
* Enclosure Design: Designing the enclosure for our device presented difficulties in fixing the dimensions accurately to accommodate all the necessary components while ensuring the device’s durability and functionality.
* PCB Design: We also faced challenges during the design of the printed circuit board (PCB) due to our limited experience in PCB design. We had to acquire new knowledge and adhere to PCB design rules to create a functional and reliable PCB for our device.
Despite these challenges, our team’s commitment to problem-solving and continuous learning allowed us to overcome each obstacle effectively. As a result, we have developed a robust and innovative solution that addresses the issues related to water tank monitoring and management, offering users a reliable and efficient way to monitor their water levels and prevent problems such as overflows and water shortages.

## Acknowledgement
We would like to express our sincere gratitude to everyone who contributed, no matter how small their role, to the successful completion of this project. Your support and assistance have been invaluable, and we appreciate your involvement in our endeavor.

We would also like to extend a special thank you to Mr. Ajith Pasqual, our module lecturer, for his guidance and mentorship throughout this project. Mr. Pasqual’s motivation and encouragement played a crucial role in inspiring us to delve into additional subjects necessary for the project’s success. Moreover, his assistance in clarifying our doubts and addressing project-related ambiguities proved to be invaluable in our journey.

Once again, thank you to all who have been a part of this project, contributing to its achievements and milestones. Your support has been truly appreciated, and it has made a significant difference in our project’s outcomes.

## References
https://www.electronicwings.com/avr-atmega/interfacing-lcd-16×2-in-4-bit-mode-with-atmega16-32-

https://www.youtube.com/watch?v=lq0R4Yz05o4

https://www.programming-electronics-diy.xyz/2021/02/playing-music-and-tones-usingpiezo.html

https://youtube.com/playlist?list=PLA6BB228B08B03EDD

https://embedds.com/programming-avr-i2c-interface/

## Team Members
Malanban K.

Manimohan T.

Madhushan R.M.S

Madusan A.K.C.S
