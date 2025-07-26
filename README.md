# 🤖 ROS 2 DOF Arm Simulation

This project simulates a simple **2-DOF robot arm** using **ROS 2**,and **Gazebo**
It demonstrates URDF modeling, joint control, and ROS-Gazebo bridge communication.

---

## 📁 Project Structure

```
arm_ws/
├── src/
│ ├── my_robot_description/ # URDF, launch, rivz
│ └── my_robot_bringup/ # config ,launch, worlds
```


---

## 🛠 Requirements

- ROS 2 Jazzy
- Gazebo Sim 
- RViz2 (for visualization)
- ros_gz_bridge 
---

## 🚀 Build & Launch

```bash
cd ~/arm_ws
colcon build
source install/setup.bash
ros2 launch my_robot_bringup arm_robot_gazebo.launch.xml

🎮 Joint Control

# If you want Move joint0 to 0.5 radians
ros2 topic pub -1 /joint0/cmd_pos std_msgs/msg/Float64 "{data: 0.5}"

# If you want Move joint1 to 1.0 radians
ros2 topic pub -1 /joint1/cmd_pos std_msgs/msg/Float64 "{data: 1.0}"

🎥 Demo

📦 Packages

    my_robot_description: URDF + xacro files

    my_robot_bringup: launch files and Gazebo bridge
