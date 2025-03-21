# Project 1: Gazebo Environment Creation

## 📍 Overview

This project involves creating a custom simulation environment using **Gazebo**, an open-source robotics simulator. The environment is designed to serve as a foundational setup for future robotics tasks such as navigation, mapping, and multi-robot coordination.

## 🧰 Tools and Technologies

- **Gazebo (Fortress / Garden / Classic)** – 3D robotics simulator  
- **ROS (optional)** – If integrated with robot control  
- **SDF/URDF** – For defining robot/environment models  
- **Custom World File** – Designed using `.world` and `.model` files  
- **RViz (optional)** – For visualization if ROS is used

## 📂 Project Structure

```
project1_gazebo_env/
├── launch/
│   └── launch_world.launch        # Launch file for starting Gazebo
├── models/
│   └── <custom_models>/           # Custom model directories
├── worlds/
│   └── custom_world.world         # Main Gazebo world file
├── scripts/
│   └── spawn_model.py             # Script to spawn models (if used)
├── README.md
```

## 🚀 How to Run

### 1. Launch the Gazebo World (Standalone)
```bash
gazebo worlds/custom_world.world
```

### 2. If Using ROS (e.g., ROS Noetic or ROS 2)
```bash
roslaunch project1_gazebo_env launch_world.launch
```

Make sure your environment variables (like `GAZEBO_MODEL_PATH`) are set properly:
```bash
export GAZEBO_MODEL_PATH=${GAZEBO_MODEL_PATH}:$(pwd)/models
```

## 🌍 World Description

The world contains:
- [x] Flat ground plane  
- [x] Obstacles (boxes, walls, ramps)  
- [x] Lighting and skybox  
- [x] Robot spawn location  
- [ ] (Optional) Predefined navigation goals  

## 📌 Notes

- Custom models are stored in the `models/` folder, each with a `model.config` and `model.sdf`.
- Modify `custom_world.world` to add more elements or change the environment layout.
- If using ROS, ensure the package is properly built and sourced using:
  ```bash
  catkin_make
  source devel/setup.bash
  ```

## ✅ To-Do

- [ ] Add more complex terrain (e.g., slopes, uneven ground)  
- [ ] Integrate SLAM-compatible robot model  
- [ ] Add sensor plugins (e.g., LIDAR, RGB camera)  
- [ ] Enable multi-robot support  
- [ ] Add automated scripts for launching and testing

## 📸 Preview

_(Insert screenshot or simulation GIF here)_

