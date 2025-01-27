# Changelog

## Unreleased

### Added
- Added in the `rb_theron_control.launch` launch file located at `rb_theron_control/launch/` some params to fix the problem with wheel movement. 
- The following params for left and right wheels has been added with the proper value in close_loop and the proper values for the PID of the joints:
    - `<param name="gazebo_ros_control/pid_gains/robot_1_right_wheel_joint/close_loop" value="position"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_right_wheel_joint/p" value="1000.0"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_right_wheel_joint/i" value="0.05"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_right_wheel_joint/d" value="0.01"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_left_wheel_joint/close_loop" value="position"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_left_wheel_joint/p" value="1000.0"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_left_wheel_joint/i" value="0.05"/>`
    - `<param name="gazebo_ros_control/pid_gains/robot_1_left_wheel_joint/d" value="0.01"/>`
- Added in the `castor.urdf.xacro` located at `rb_theron_description/urdf/wheels` the configuration required in the joints config.
- Added in the `rubber_wheel.urdf.xacro` located at `rb_theron_description/urdf/wheels` the configuration required in the joints config.

### Removed
- Removed RealSense (`sensor_intel_d435`, lines 62 to 68) from the `rb_theron.urdf.xacro` located at `rb_theron_description/robots/`.

## [0.1.0] 2024-01-29

### Added
- Added use of ExtendedArgument and AddArgumentParser in `rb_theron_localization` launch files.
- Added use of ExtendedArgument and AddArgumentParser in `rb_theron_navigation` launch files.
- Added global frame in `rb_theron_localization` and `rb_theron_navigation` launch files.
- Added output topic prefix in `rb_theron_localization` launch files.
- Added `rb_theron_navigation_private` to separate public from private navigation packages.
- Added `rb_theron_common_private` to separate public from private common packages used for robot control and simulation.
- Separated move from safety controller in `rb_theron_navigation_private`.
- Added install directories in the `CMakeLists.txt` of the `rb_theron_description`.
- Added `use_sim` variable for castor wheel simulation in the `rb_theron_description`.
- Use v4 theron base as standard in the `rb_theron_description`.
- Added `diff_drive_controller` dependency with diff controller in the `package.xml` of the `rb_theron_control`.
- Created readme file.
- Created changelog file.

### Removed
- Removed unused modules in the `rb_theron_localization` launch files.
- Removed unneeded params in `rb_theron_localization` and `rb_theron_navigation` launch files.
- Removed private dependencies from `package.xml` of the `rb_theron_navigation`.
- Removed private call to `rb_theron_navigation` in the `navigation _complete.launch`file.
- Removed private dependencies from `package.xml` of the `rb_theron_common`.
- Deleted `testing` file as unnecessary.

### Changed
- Launched map server now on the robot namespace in the `rb_theron_localization` map_server launch file.
- Corrected python syntax in the `rb_theron_localization` launch files.
- Improved readability and code of the `rb_theron_localization` files.
- Moved `localization.launch.py` to `amcl.launch.py` in the `rb_theron_localization`.
- Corrected python syntax in the `rb_theron_navigation` launch files.
- Improved readability and code of the `rb_theron_navigation` files.
- Changed launch of `rb_theron_navigation` to separate public from private navigation packages.
- Correct castor wheel for simulation in Noetic of the `rb_theron_description`.
- Updated inertias in rb_theron wheels for better performance in the urdf files of the `rb_theron_description`.
- Corrected harcoded ros_control robot description in the robots and urdf files of the `rb_theron_description`.
- Set caster wheel as fixed joint in the urdf files of the `rb_theron_description`.
- Modify teb_local_planner_params for omni use in the `rb_theron_navigation` launch files.
- Corrected the yaml syntax of config files from the `rb_theron_control`.
- Changed tf frequency from 100Hz to 20Hz in the config file of `rb_theron_control`.




