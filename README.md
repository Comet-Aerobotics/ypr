# Instructions to Run

1. Insert this file into the Home portion of the file manager <br/>
2. Navigate into the ros2_ws using <br/> ``` cd ros2_ws ```
3. Run colcon build <br/> ```colcon build```
   
4. Source the setup <br/> ```source install/setup.bash```

5. Build the package <br/> ```colcon build --packages-select vector```
6. Give the USB connection permissions using <br/> ```sudo chmod 666 /dev/ttyUSB0```

7. Now we run it with <br/> ```ros2 run vector vector /dev/ttyUSB0```

8. To check that your ypr is being published, you can run ```ros2 topic echo /vector_ypr```.


> [!IMPORTANT]
> This is for Ubuntu Jammy Jellyfish, and you need to already have ros2 installed on your machine

We are using [ROS Humble](https://docs.ros.org/en/humble/Installation.html)

# Foxglove Instructions

1. Install Foxglove by following instructions on this website: https://foxglove.dev/download
2. Click "Open connection", and then ensure "Rosbridge" is selected. Click open.

3. Assuming you've completed the above "Instructions to Run", in one terminal run ```ros2 run rosapi rosapi_node```.
4. In another, ensure you are in the `ros2_ws/ros2_ws` folder, and run ```ros2 run rosbridge_server rosbridge_websocket```.

5. In Foxglove, find your Panel window. Make sure your Plot window is open. Under the Series tab, clear "Message path" on "Pitch", "Roll", & "Yaw", and enter `/vector_ypr.#`, replacing # with x, y, and z appropriately. Your data should begin to plot!
