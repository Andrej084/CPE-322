Terminal 1- MQTT
Andrejs-MBP:lesson5 andrejthekoolaidman$ mosquitto_sub -h localhost -v -t test/topic
test/topic Hello
^C
Andrejs-MBP:lesson5 andrejthekoolaidman$


Terminal 2-MQTT
Andrejs-MBP:lesson5 andrejthekoolaidman$ mosquitto_pub -h localhost -t test/topic -m "Hello"
Andrejs-MBP:lesson5 andrejthekoolaidman$

Terminal 1 (sub.py)
Andrejs-MBP:lesson5 andrejthekoolaidman$ python sub.py
Connected with result code 0
paho/test Hello

Terminal 2(sub.py)
Andrejs-MBP:lesson5 andrejthekoolaidman$ python pub.py
Andrejs-MBP:lesson5 andrejthekoolaidman$

Terminal 1
Andrejs-MBP:lesson5 andrejthekoolaidman$ python sub_multiple.py
Connected with result code 0
paho/test/multiple multiple 1
paho/test/multiple multiple 2

Terminal 2
Andrejs-MBP:lesson5 andrejthekoolaidman$ python pub_multiple.py
Andrejs-MBP:lesson5 andrejthekoolaidman$


Andrejs-MBP:lesson5 andrejthekoolaidman$ python pubcpu.py
2025-04-27 23:52:57
CPU Usage:    14.3 %
2025-05-12 23:53:07
CPU Usage:    10.7 %
2025-05-12 23:53:17
CPU Usage:     8.6 %
2025-05-12 23:53:27
CPU Usage:     6.5 %
Andrejs-MBP:lesson5 andrejthekoolaidman$
