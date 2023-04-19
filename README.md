# Use [piksi_multi_cpp](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_multi_cpp) with ROS noetic and Piksi Multi Firmware 2.4.20
Please use the new piksi_multi_cpp driver. The Python driver is not maintained and outdated. If you still want to use the Python driver checkout release [v1.10.0](https://github.com/ethz-asl/ethz_piksi_ros/tree/v1.11.0).

Instructions
------

```
- git clone git@github.com:ori-drs/ethz_piksi_ros.git
- git clone git@github.com:ethz-asl/libserialport_catkin.git
- git clone git@github.com:ethz-asl/libsbp_catkin.git
- catkin build piksi_multi_cpp
- roslaunch piksi_multi_cpp rover.launch  #if using the rover only
```

Overview
------
- [piksi_multi_rtk_ros](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_multi_rtk_ros): ROS driver for Piksi RTK receiver device, hardware version [Multi](https://www.swiftnav.com/piksi-multi).
- [piksi_rtk_kml](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_rtk_kml): ROS node to generate KML files (Keyhole Markup Language) from Piksi messages. These files can be visualized in Google Earth.
- [piksi_rtk_msgs](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_rtk_msgs): ROS messages used by the driver(s).
- [piksi_v2_rtk_ros](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_v2_rtk_ros): ROS driver for Piksi RTK receiver device, hardware version [V2](http://docs.swiftnav.com/pdfs/piksi_datasheet_v2.3.1.pdf). **Discontinued**
- [rqt_gps_rtk_plugin](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/rqt_gps_rtk_plugin): Graphical User Interface to check the status of RTK fix. This gui is implemented wit [Qt](https://wiki.qt.io/Install_Qt_5_on_Ubuntu) such that it may be added to your preferred rqt perspective.
- [utils](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/utils): collection of configurations and useful scripts. This folder contains [piksi_rtklib_postp](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/utils/piksi_rtklib_postp) which can be used to obtained post processed RTK positions using only Piksi Multi for data collection (i.e. a base station is not needed). See the corresponding [wiki page](https://github.com/ethz-asl/ethz_piksi_ros/wiki/Data-collection-and-post-processing).

Impatient Users
------
### Piksi Multi
RTK fix obtained in average in 3 minutes.
 - [Install Piksi Multi ROS Driver](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_multi_rtk_ros#installation-and-configuration).
 - [Configure Your Piksi Multi](https://github.com/ethz-asl/ethz_piksi_ros/wiki/Installing-and-Configuring-Your-Piksi).
 - [Example Launch Files](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_multi_rtk_ros/launch).
  
### Piksi V2 (Discontinued)
RTK fix obtained in average in 10 minutes.
 - [Install Piksi V2 ROS Driver](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_v2_rtk_ros#installation-and-configuration).
 - [Configure Your Piksi V2](https://github.com/ethz-asl/ethz_piksi_ros/wiki/Installing-and-Configuring-Your-Piksi).
 - [Example Launch Files](https://github.com/ethz-asl/ethz_piksi_ros/tree/master/piksi_v2_rtk_ros/launch).

License
-------
The source code is released under a [BSD 3-Clause license](https://github.com/ethz-asl/ethz_piksi_ros/blob/master/LICENSE).

Build Status
-------
[![Build Status](https://ci.leggedrobotics.com/buildStatus/icon?job=github_ethz-asl/ethz_piksi_ros/master)](https://ci.leggedrobotics.com/job/github_ethz-asl/job/ethz_piksi_ros/job/master/)

Credits
-------
Marco Tranzatto, Kai Holtmann, Michael Pantic, Rik Baehnemann - ETHZ ASL & RSL - 28 April 2019

Based on the initial work of Daniel Eckert.


Bugs & Feature Requests
-------
Please report bugs and request features using the [Issue Tracker](https://github.com/ethz-asl/ethz_piksi_ros/issues).

Before reporting a mulfunction in the driver, please have a look at the [Frequently Asked Questions (FAQ)](https://github.com/ethz-asl/ethz_piksi_ros/wiki/FAQ).

**Related projects**
-------
Browser Online Visualization [https://github.com/ziliHarvey/GPS-Browser-Visualizer](https://github.com/ziliHarvey/GPS-Browser-Visualizer)<br>
RVIZ Online Visualization [https://github.com/nobleo/rviz_satellite](https://github.com/nobleo/rviz_satellite)
