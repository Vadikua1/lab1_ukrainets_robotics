# Lab 1: Building Robot in Gazebo


### 1. Clone Repository

```bash
cd ~
git clone https://github.com/Vadikua1/lab1_ukrainets_robotics.git
cd lab1_ukrainets_robotics
```

### 2. Build Docker Image

```bash
./scripts/cmd build-docker
```

This takes 10-15 minutes on first run.

### 3. Install and open VScode

```bash
code .
```

### 4. Run Container

```bash
./scripts/cmd run
```

### 4. Run Gazebo

```bash
gz sim /opt/ws/src/code/lab1/worlds/robot.sdf
```

### 5. In another terminal run next code to run our robot

```bash
gz topic -t "/cmd_vel" -m gz.msgs.Twist -p "linear: {x: 0.5}, angular: {z: 0.05}"
```

Don't forget run the simulation.

### 5. In another terminal run this code for gathering data from Lidar

```bash
gz topic -e -t /lidar
```

