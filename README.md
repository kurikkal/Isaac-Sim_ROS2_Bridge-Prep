# Isaac-Sim_ROS2_Bridge-Prep


As of now in the latest released version of Isaac Sim(2022.2.0), the ROS2 Bridge only supports ROS2 Foxy(which only runs on Ubuntu 20.04). The problem will be resolved in the next release of Isaac Sim.


## Step 1
Move the 'fastdds.xml' file also located at the root of the ros2_workspace folder in Isaac Sim folder to '~/.ros/'

## Step 2
Open the terminal and Run:
```
unset LD_LIBRARY_PATH
export FASTRTPS_DEFAULT_PROFILES_FILE=~/.ros/fastdds.xml
export ROS_DOMAIN_ID=(id_number)
```

Choose a domain ID(eg:99)

## Step 3
Launch Isaac Sim

IMP: Do not source ROS2 in the terminal running Isaac Sim. So do not add the command to source ROS2 and the command to set ROS2 Domain ID to ~/.bashrc file.

## Step 3
After Isaac Sim is launched. Enable ROS2 Bridge in Isaac Sim ' Windows/Extensions'. ROS Bridge is enabled on default. It should be disabled first.

## Step 4
Open action graph. Search for ROS2 Context and drag it into the empty graph. Type the same domain ID you choose in the node. Edit the rest of the action graph according to the project.

## Step 5
 Go to the terminal in Step 3, Source ROS2 there:
 ```
 source /opt/ros/foxy/setup.bash
 
 ```
 
 Now the bridge connection is established.
