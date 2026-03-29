# waver_ws

ROS2 Humble 기반 Waver Gazebo / SLAM / Navigation / Patrol 실행 방법

---

 Gazebo 실행 (모델 스폰)

```bash
cd ~/waver_ws
source /opt/ros/humble/setup.bash
colcon build --symlink-install --packages-skip teb_local_planner
source ~/waver_ws/install/setup.bash
ros2 launch waver_description gazebo.launch.py
```

---

Mapping (SLAM)

```bash
cd ~/waver_ws
source /opt/ros/humble/setup.bash
colcon build --symlink-install --packages-skip teb_local_planner
source ~/waver_ws/install/setup.bash
ros2 launch ugv_slam waver_gmapping.launch.py
```

---

 Navigation

```bash
cd ~/waver_ws
source /opt/ros/humble/setup.bash
colcon build --symlink-install --packages-skip teb_local_planner
source ~/waver_ws/install/setup.bash
ros2 launch ugv_nav waver_nav.launch.py
```

---

## SLAM + Navigation

```bash
cd ~/waver_ws
source /opt/ros/humble/setup.bash
colcon build --symlink-install --packages-skip teb_local_planner
source ~/waver_ws/install/setup.bash
ros2 launch ugv_nav waver_slam_nav.launch.py
```

---

## Patrol (웨이포인트 순찰)

```bash
cd ~/waver_ws
source /opt/ros/humble/setup.bash
colcon build --symlink-install --packages-skip teb_local_planner
source ~/waver_ws/install/setup.bash
ros2 launch my_waver_app patrol.launch.py
```
