Kinect can be used to get pseudo laserScans using 

```sh
rosrun depthimage_to_laserscan depthimage_to_laserscan image:=/camera/depth_registered/image_raw
```

Run freenect.launch

```sh
roslaunch freenect_launch freenect.launch depth_registration:=true
```

Run the rtabmap node

```sh
roslaunch rtabmap_ros rtabmap.launch rtabmap_args:="--delete_db_on_start" rviz:=true rtabmapviz:=false
```

To use the saved config for RViz
```sh
rviz -d ~/.ros/nav.rviz
```

Laserscan working through Kinect. Explore ways to use this laserscan for autonomous navigation