# Zenbedded minimal application

Minimal repo with Zenbedded fetched as a Zephyr module. Based on the `rcl_e2e` test.

Least friction - use [IDE for Zephyr](https://docs.zephyrproject.org/latest/develop/tools/ide_for_zephyr_vscode_ext.html) and have `ros-<DISTRO>-rmw-zenoh-cpp` installed. After build, run the zenoh router:

```bash
ros2 run rmw_zenoh_cpp rmw_zenohd
```

and then the Zephyr executable:


```bash
./zenbedded_demo_tier1/build/native_sim/native/64/zephyr/zephyr.exe
```

and then you can read the data incoming on the `/joint_states` topic directly for tier1 transport:

```bash
ros2 topic echo /joint_states sensor_msgs/msg/JointState
```
