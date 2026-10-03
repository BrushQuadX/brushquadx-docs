.. _future:

Future Work
============

1. Integrate IMU readings towards VisionOTG to see the orientation and tilt of the drone
    - Separate thread for capturing and displaying drone orientation
    - Integrate roll, pitch, yaw + horizon telemetry visualizations
    - treat drone NRF24L01 as a duplex by receiving controller commands and transmitting IMU readings
2. Improve model inference time since ONNX model has high latency
    - optimize the model through quantization and use `ncnn` rust package for running inference
    - Utilize model accelerators for the Raspberry Pi
3. Integrate model segmentation for segmenting detected objects
4. `Oswell Avatar/AI <https://github.com/JohnMVSantos/OswelM>`_ integration / drawing
5. Design ESP32-based brush drone schematic and implement systemctl services
    - systemctl status visionOTG
    - systemctl status droneControl -> adds a service for controlling the drone
    - Raspberry Pi 5 interface for the controller
    - Custom PCB for Raspberry Pi 5 Joystick + power connections + LCD for display
    - NRF24L01 readings published towards VisionOTG Zenohd topics