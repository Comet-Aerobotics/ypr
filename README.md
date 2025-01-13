# Instructions to Run

1. Insert this file into the Home portion of the file manager <br/>
2. Navigate into the ros2_ws using <br/> ``` cd ros2_ws ```
3. Run colcon build <br/> ```colcon build```
   
4. Source the setup <br/> ```source install/setup.bash```
5. Build the package <br/> ```colcon build --packages-select vector```
6. Give the USB connection permissions using <br/> ```sudo chmod 666 /dev/ttyUSB0```
7. Now we run it with <br/> ```ros2 run vector vector /dev/ttyUSB0```


> [!IMPORTANT]
> This is for Ubuntu Jammy Jellyfish, and you need to already have ros2 installed on your machine

We are using [ROS Humble](https://docs.ros.org/en/humble/Installation.html)

