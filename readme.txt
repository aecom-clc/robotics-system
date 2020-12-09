(build not in docker, but in an conda environment with python 2.7 and ROS melodic installed)
(ref only, not in exact because in conda environment) /sharedVol/aec/ros/robotics_system_js/ros/catkin_ws_rosbridge$ 
catkin clean -b
catkin build
source devel/setup.bash
roslaunch robot_gui_bridge websocket.launch

rostopic echo /cmd_vel

///////////////////////////////////////////
// origin (seems updated, this is just an outdated reference)

aibd@ebc88db71dd6:/sharedVol/aec/ros$ tree -L 1
.
├── catkin_ws_rosbridge
├── readme
└── robotics_system_js

///////////////////////////////////////////
// ref

https://www.robosynthesis.com/post/ros-web-tutorial-part-1-rosbridge-server-and-roslibjs

aibd@ebc88db71dd6:/sharedVol/aec/ros$ tree
.
├── catkin_ws_rosbridge
│   ├── build
│   │   ├── catkin_tools_prebuild
│   │   │   ├── CMakeCache.txt
│   │   │   ├── CMakeFiles
│   │   │   │   ├── 3.10.2
│   │   │   │   │   ├── CMakeCCompiler.cmake
│   │   │   │   │   ├── CMakeCXXCompiler.cmake
│   │   │   │   │   ├── CMakeDetermineCompilerABI_C.bin
│   │   │   │   │   ├── CMakeDetermineCompilerABI_CXX.bin
│   │   │   │   │   ├── CMakeSystem.cmake
│   │   │   │   │   ├── CompilerIdC
│   │   │   │   │   │   ├── CMakeCCompilerId.c
│   │   │   │   │   │   ├── a.out
│   │   │   │   │   │   └── tmp
│   │   │   │   │   └── CompilerIdCXX
│   │   │   │   │       ├── CMakeCXXCompilerId.cpp
│   │   │   │   │       ├── a.out
│   │   │   │   │       └── tmp
│   │   │   │   ├── CMakeDirectoryInformation.cmake
│   │   │   │   ├── CMakeError.log
│   │   │   │   ├── CMakeOutput.log
│   │   │   │   ├── CMakeRuleHashes.txt
│   │   │   │   ├── CMakeTmp
│   │   │   │   ├── Makefile.cmake
│   │   │   │   ├── Makefile2
│   │   │   │   ├── TargetDirectories.txt
│   │   │   │   ├── _catkin_empty_exported_target.dir
│   │   │   │   │   ├── DependInfo.cmake
│   │   │   │   │   ├── build.make
│   │   │   │   │   ├── cmake_clean.cmake
│   │   │   │   │   └── progress.make
│   │   │   │   ├── clean_test_results.dir
│   │   │   │   │   ├── DependInfo.cmake
│   │   │   │   │   ├── build.make
│   │   │   │   │   ├── cmake_clean.cmake
│   │   │   │   │   └── progress.make
│   │   │   │   ├── cmake.check_cache
│   │   │   │   ├── download_extra_data.dir
│   │   │   │   │   ├── DependInfo.cmake
│   │   │   │   │   ├── build.make
│   │   │   │   │   ├── cmake_clean.cmake
│   │   │   │   │   └── progress.make
│   │   │   │   ├── doxygen.dir
│   │   │   │   │   ├── DependInfo.cmake
│   │   │   │   │   ├── build.make
│   │   │   │   │   ├── cmake_clean.cmake
│   │   │   │   │   └── progress.make
│   │   │   │   ├── feature_tests.bin
│   │   │   │   ├── feature_tests.c
│   │   │   │   ├── feature_tests.cxx
│   │   │   │   ├── progress.marks
│   │   │   │   ├── run_tests.dir
│   │   │   │   │   ├── DependInfo.cmake
│   │   │   │   │   ├── build.make
│   │   │   │   │   ├── cmake_clean.cmake
│   │   │   │   │   └── progress.make
│   │   │   │   └── tests.dir
│   │   │   │       ├── DependInfo.cmake
│   │   │   │       ├── build.make
│   │   │   │       ├── cmake_clean.cmake
│   │   │   │       └── progress.make
│   │   │   ├── CMakeLists.txt
│   │   │   ├── CTestConfiguration.ini
│   │   │   ├── CTestCustom.cmake
│   │   │   ├── CTestTestfile.cmake
│   │   │   ├── Makefile
│   │   │   ├── atomic_configure
│   │   │   │   ├── _setup_util.py
│   │   │   │   ├── env.sh
│   │   │   │   ├── local_setup.bash
│   │   │   │   ├── local_setup.sh
│   │   │   │   ├── local_setup.zsh
│   │   │   │   ├── setup.bash
│   │   │   │   ├── setup.sh
│   │   │   │   └── setup.zsh
│   │   │   ├── catkin
│   │   │   │   └── catkin_generated
│   │   │   │       └── version
│   │   │   │           └── package.cmake
│   │   │   ├── catkin_generated
│   │   │   │   ├── env_cached.sh
│   │   │   │   ├── generate_cached_setup.py
│   │   │   │   ├── installspace
│   │   │   │   │   ├── _setup_util.py
│   │   │   │   │   ├── catkin_tools_prebuild.pc
│   │   │   │   │   ├── catkin_tools_prebuildConfig-version.cmake
│   │   │   │   │   ├── catkin_tools_prebuildConfig.cmake
│   │   │   │   │   ├── env.sh
│   │   │   │   │   ├── local_setup.bash
│   │   │   │   │   ├── local_setup.sh
│   │   │   │   │   ├── local_setup.zsh
│   │   │   │   │   ├── setup.bash
│   │   │   │   │   ├── setup.sh
│   │   │   │   │   └── setup.zsh
│   │   │   │   ├── package.cmake
│   │   │   │   ├── pkg.develspace.context.pc.py
│   │   │   │   ├── pkg.installspace.context.pc.py
│   │   │   │   ├── setup_cached.sh
│   │   │   │   └── stamps
│   │   │   │       └── catkin_tools_prebuild
│   │   │   │           ├── _setup_util.py.stamp
│   │   │   │           ├── interrogate_setup_dot_py.py.stamp
│   │   │   │           ├── package.xml.stamp
│   │   │   │           └── pkg.pc.em.stamp
│   │   │   ├── cmake_install.cmake
│   │   │   ├── gtest
│   │   │   │   ├── CMakeFiles
│   │   │   │   │   ├── CMakeDirectoryInformation.cmake
│   │   │   │   │   └── progress.marks
│   │   │   │   ├── CTestTestfile.cmake
│   │   │   │   ├── Makefile
│   │   │   │   ├── cmake_install.cmake
│   │   │   │   └── googlemock
│   │   │   │       ├── CMakeFiles
│   │   │   │       │   ├── CMakeDirectoryInformation.cmake
│   │   │   │       │   ├── gmock.dir
│   │   │   │       │   │   ├── DependInfo.cmake
│   │   │   │       │   │   ├── __
│   │   │   │       │   │   │   └── googletest
│   │   │   │       │   │   │       └── src
│   │   │   │       │   │   ├── build.make
│   │   │   │       │   │   ├── cmake_clean.cmake
│   │   │   │       │   │   ├── depend.make
│   │   │   │       │   │   ├── flags.make
│   │   │   │       │   │   ├── link.txt
│   │   │   │       │   │   ├── progress.make
│   │   │   │       │   │   └── src
│   │   │   │       │   ├── gmock_main.dir
│   │   │   │       │   │   ├── DependInfo.cmake
│   │   │   │       │   │   ├── __
│   │   │   │       │   │   │   └── googletest
│   │   │   │       │   │   │       └── src
│   │   │   │       │   │   ├── build.make
│   │   │   │       │   │   ├── cmake_clean.cmake
│   │   │   │       │   │   ├── depend.make
│   │   │   │       │   │   ├── flags.make
│   │   │   │       │   │   ├── link.txt
│   │   │   │       │   │   ├── progress.make
│   │   │   │       │   │   └── src
│   │   │   │       │   └── progress.marks
│   │   │   │       ├── CTestTestfile.cmake
│   │   │   │       ├── Makefile
│   │   │   │       ├── cmake_install.cmake
│   │   │   │       └── gtest
│   │   │   │           ├── CMakeFiles
│   │   │   │           │   ├── CMakeDirectoryInformation.cmake
│   │   │   │           │   ├── gtest.dir
│   │   │   │           │   │   ├── DependInfo.cmake
│   │   │   │           │   │   ├── build.make
│   │   │   │           │   │   ├── cmake_clean.cmake
│   │   │   │           │   │   ├── depend.make
│   │   │   │           │   │   ├── flags.make
│   │   │   │           │   │   ├── link.txt
│   │   │   │           │   │   ├── progress.make
│   │   │   │           │   │   └── src
│   │   │   │           │   ├── gtest_main.dir
│   │   │   │           │   │   ├── DependInfo.cmake
│   │   │   │           │   │   ├── build.make
│   │   │   │           │   │   ├── cmake_clean.cmake
│   │   │   │           │   │   ├── depend.make
│   │   │   │           │   │   ├── flags.make
│   │   │   │           │   │   ├── link.txt
│   │   │   │           │   │   ├── progress.make
│   │   │   │           │   │   └── src
│   │   │   │           │   └── progress.marks
│   │   │   │           ├── CTestTestfile.cmake
│   │   │   │           ├── Makefile
│   │   │   │           └── cmake_install.cmake
│   │   │   ├── package.xml
│   │   │   └── test_results
│   │   └── robot_gui_bridge
│   │       ├── CATKIN_IGNORE
│   │       ├── CMakeCache.txt
│   │       ├── CMakeFiles
│   │       │   ├── 3.10.2
│   │       │   │   ├── CMakeCCompiler.cmake
│   │       │   │   ├── CMakeCXXCompiler.cmake
│   │       │   │   ├── CMakeDetermineCompilerABI_C.bin
│   │       │   │   ├── CMakeDetermineCompilerABI_CXX.bin
│   │       │   │   ├── CMakeSystem.cmake
│   │       │   │   ├── CompilerIdC
│   │       │   │   │   ├── CMakeCCompilerId.c
│   │       │   │   │   ├── a.out
│   │       │   │   │   └── tmp
│   │       │   │   └── CompilerIdCXX
│   │       │   │       ├── CMakeCXXCompilerId.cpp
│   │       │   │       ├── a.out
│   │       │   │       └── tmp
│   │       │   ├── CMakeDirectoryInformation.cmake
│   │       │   ├── CMakeError.log
│   │       │   ├── CMakeOutput.log
│   │       │   ├── CMakeRuleHashes.txt
│   │       │   ├── CMakeTmp
│   │       │   ├── Makefile.cmake
│   │       │   ├── Makefile2
│   │       │   ├── TargetDirectories.txt
│   │       │   ├── _catkin_empty_exported_target.dir
│   │       │   │   ├── DependInfo.cmake
│   │       │   │   ├── build.make
│   │       │   │   ├── cmake_clean.cmake
│   │       │   │   └── progress.make
│   │       │   ├── clean_test_results.dir
│   │       │   │   ├── DependInfo.cmake
│   │       │   │   ├── build.make
│   │       │   │   ├── cmake_clean.cmake
│   │       │   │   └── progress.make
│   │       │   ├── cmake.check_cache
│   │       │   ├── download_extra_data.dir
│   │       │   │   ├── DependInfo.cmake
│   │       │   │   ├── build.make
│   │       │   │   ├── cmake_clean.cmake
│   │       │   │   └── progress.make
│   │       │   ├── doxygen.dir
│   │       │   │   ├── DependInfo.cmake
│   │       │   │   ├── build.make
│   │       │   │   ├── cmake_clean.cmake
│   │       │   │   └── progress.make
│   │       │   ├── feature_tests.bin
│   │       │   ├── feature_tests.c
│   │       │   ├── feature_tests.cxx
│   │       │   ├── progress.marks
│   │       │   ├── run_tests.dir
│   │       │   │   ├── DependInfo.cmake
│   │       │   │   ├── build.make
│   │       │   │   ├── cmake_clean.cmake
│   │       │   │   └── progress.make
│   │       │   └── tests.dir
│   │       │       ├── DependInfo.cmake
│   │       │       ├── build.make
│   │       │       ├── cmake_clean.cmake
│   │       │       └── progress.make
│   │       ├── CTestConfiguration.ini
│   │       ├── CTestCustom.cmake
│   │       ├── CTestTestfile.cmake
│   │       ├── Makefile
│   │       ├── atomic_configure
│   │       │   ├── _setup_util.py
│   │       │   ├── env.sh
│   │       │   ├── local_setup.bash
│   │       │   ├── local_setup.sh
│   │       │   ├── local_setup.zsh
│   │       │   ├── setup.bash
│   │       │   ├── setup.sh
│   │       │   └── setup.zsh
│   │       ├── catkin
│   │       │   └── catkin_generated
│   │       │       └── version
│   │       │           └── package.cmake
│   │       ├── catkin_generated
│   │       │   ├── env_cached.sh
│   │       │   ├── generate_cached_setup.py
│   │       │   ├── installspace
│   │       │   │   ├── _setup_util.py
│   │       │   │   ├── env.sh
│   │       │   │   ├── local_setup.bash
│   │       │   │   ├── local_setup.sh
│   │       │   │   ├── local_setup.zsh
│   │       │   │   ├── robot_gui_bridge.pc
│   │       │   │   ├── robot_gui_bridgeConfig-version.cmake
│   │       │   │   ├── robot_gui_bridgeConfig.cmake
│   │       │   │   ├── setup.bash
│   │       │   │   ├── setup.sh
│   │       │   │   └── setup.zsh
│   │       │   ├── package.cmake
│   │       │   ├── pkg.develspace.context.pc.py
│   │       │   ├── pkg.installspace.context.pc.py
│   │       │   ├── setup_cached.sh
│   │       │   └── stamps
│   │       │       └── robot_gui_bridge
│   │       │           ├── _setup_util.py.stamp
│   │       │           ├── interrogate_setup_dot_py.py.stamp
│   │       │           ├── package.xml.stamp
│   │       │           └── pkg.pc.em.stamp
│   │       ├── cmake_install.cmake
│   │       ├── gtest
│   │       │   ├── CMakeFiles
│   │       │   │   ├── CMakeDirectoryInformation.cmake
│   │       │   │   └── progress.marks
│   │       │   ├── CTestTestfile.cmake
│   │       │   ├── Makefile
│   │       │   ├── cmake_install.cmake
│   │       │   └── googlemock
│   │       │       ├── CMakeFiles
│   │       │       │   ├── CMakeDirectoryInformation.cmake
│   │       │       │   ├── gmock.dir
│   │       │       │   │   ├── DependInfo.cmake
│   │       │       │   │   ├── __
│   │       │       │   │   │   └── googletest
│   │       │       │   │   │       └── src
│   │       │       │   │   ├── build.make
│   │       │       │   │   ├── cmake_clean.cmake
│   │       │       │   │   ├── depend.make
│   │       │       │   │   ├── flags.make
│   │       │       │   │   ├── link.txt
│   │       │       │   │   ├── progress.make
│   │       │       │   │   └── src
│   │       │       │   ├── gmock_main.dir
│   │       │       │   │   ├── DependInfo.cmake
│   │       │       │   │   ├── __
│   │       │       │   │   │   └── googletest
│   │       │       │   │   │       └── src
│   │       │       │   │   ├── build.make
│   │       │       │   │   ├── cmake_clean.cmake
│   │       │       │   │   ├── depend.make
│   │       │       │   │   ├── flags.make
│   │       │       │   │   ├── link.txt
│   │       │       │   │   ├── progress.make
│   │       │       │   │   └── src
│   │       │       │   └── progress.marks
│   │       │       ├── CTestTestfile.cmake
│   │       │       ├── Makefile
│   │       │       ├── cmake_install.cmake
│   │       │       └── gtest
│   │       │           ├── CMakeFiles
│   │       │           │   ├── CMakeDirectoryInformation.cmake
│   │       │           │   ├── gtest.dir
│   │       │           │   │   ├── DependInfo.cmake
│   │       │           │   │   ├── build.make
│   │       │           │   │   ├── cmake_clean.cmake
│   │       │           │   │   ├── depend.make
│   │       │           │   │   ├── flags.make
│   │       │           │   │   ├── link.txt
│   │       │           │   │   ├── progress.make
│   │       │           │   │   └── src
│   │       │           │   ├── gtest_main.dir
│   │       │           │   │   ├── DependInfo.cmake
│   │       │           │   │   ├── build.make
│   │       │           │   │   ├── cmake_clean.cmake
│   │       │           │   │   ├── depend.make
│   │       │           │   │   ├── flags.make
│   │       │           │   │   ├── link.txt
│   │       │           │   │   ├── progress.make
│   │       │           │   │   └── src
│   │       │           │   └── progress.marks
│   │       │           ├── CTestTestfile.cmake
│   │       │           ├── Makefile
│   │       │           └── cmake_install.cmake
│   │       └── test_results
│   ├── devel
│   │   ├── _setup_util.py -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/_setup_util.py
│   │   ├── cmake.lock -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/cmake.lock
│   │   ├── env.sh -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/env.sh
│   │   ├── etc
│   │   │   └── catkin
│   │   │       └── profile.d
│   │   │           └── 06-ctr-nuke.sh
│   │   ├── lib
│   │   │   └── pkgconfig
│   │   │       ├── catkin_tools_prebuild.pc -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/lib/pkgconfig/catkin_tools_prebuild.pc
│   │   │       └── robot_gui_bridge.pc -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/robot_gui_bridge/lib/pkgconfig/robot_gui_bridge.pc
│   │   ├── local_setup.bash -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/local_setup.bash
│   │   ├── local_setup.sh -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/local_setup.sh
│   │   ├── local_setup.zsh -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/local_setup.zsh
│   │   ├── setup.bash -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/setup.bash
│   │   ├── setup.sh -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/setup.sh
│   │   ├── setup.zsh -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/setup.zsh
│   │   └── share
│   │       ├── catkin_tools_prebuild
│   │       │   └── cmake
│   │       │       ├── catkin_tools_prebuildConfig-version.cmake -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/share/catkin_tools_prebuild/cmake/catkin_tools_prebuildConfig-version.cmake
│   │       │       └── catkin_tools_prebuildConfig.cmake -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/catkin_tools_prebuild/share/catkin_tools_prebuild/cmake/catkin_tools_prebuildConfig.cmake
│   │       └── robot_gui_bridge
│   │           └── cmake
│   │               ├── robot_gui_bridgeConfig-version.cmake -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/robot_gui_bridge/share/robot_gui_bridge/cmake/robot_gui_bridgeConfig-version.cmake
│   │               └── robot_gui_bridgeConfig.cmake -> /sharedVol/docker/sharedVol/aec/ros/catkin_ws_rosbridge/devel/.private/robot_gui_bridge/share/robot_gui_bridge/cmake/robot_gui_bridgeConfig.cmake
│   ├── logs
│   │   ├── catkin_tools_prebuild
│   │   │   ├── build.cache-manifest.000.log
│   │   │   ├── build.cache-manifest.log
│   │   │   ├── build.cmake.000.log
│   │   │   ├── build.cmake.log
│   │   │   ├── build.ctr-nuke.000.log
│   │   │   ├── build.ctr-nuke.log
│   │   │   ├── build.loadenv.000.log
│   │   │   ├── build.loadenv.log
│   │   │   ├── build.make.000.log
│   │   │   ├── build.make.log
│   │   │   ├── build.mkdir.000.log
│   │   │   ├── build.mkdir.001.log
│   │   │   ├── build.mkdir.log
│   │   │   ├── build.symlink.000.log
│   │   │   └── build.symlink.log
│   │   └── robot_gui_bridge
│   │       ├── build.cache-manifest.000.log
│   │       ├── build.cache-manifest.log
│   │       ├── build.cmake.000.log
│   │       ├── build.cmake.log
│   │       ├── build.ctr-nuke.000.log
│   │       ├── build.ctr-nuke.log
│   │       ├── build.loadenv.000.log
│   │       ├── build.loadenv.log
│   │       ├── build.make.000.log
│   │       ├── build.make.log
│   │       ├── build.mkdir.000.log
│   │       ├── build.mkdir.001.log
│   │       ├── build.mkdir.log
│   │       ├── build.symlink.000.log
│   │       └── build.symlink.log
│   └── src
│       ├── CMakeLists.txt -> /opt/ros/melodic/share/catkin/cmake/toplevel.cmake
│       └── robot_gui_bridge
│           ├── CMakeLists.txt
│           ├── gui
│           │   └── gui.html
│           ├── launch
│           │   └── websocket.launch
│           └── package.xml
├── readme
└── robotics_system_js
    ├── ros
    │   ├── aecom.css
    │   ├── css
    │   │   ├── live.css
    │   │   └── recoder.css
    │   ├── demo
    │   │   ├── demo-hls.html
    │   │   ├── demo-live (another copy).html
    │   │   ├── demo-live (copy).html
    │   │   ├── demo-monitor.html
    │   │   ├── demo-monitorsplit.html
    │   │   ├── demo-rtmp.html
    │   │   ├── demo-ui-voice.html
    │   │   ├── imgs
    │   │   │   └── 1.jpg
    │   │   └── index.html
    │   ├── index.html
    │   ├── js
    │   │   ├── ckplayer
    │   │   │   ├── ckplayer.js
    │   │   │   ├── ckplayer.swf
    │   │   │   ├── ckplayer.xml
    │   │   │   ├── language.xml
    │   │   │   ├── m3u8.swf
    │   │   │   ├── related.xml
    │   │   │   ├── share
    │   │   │   │   ├── feixin.png
    │   │   │   │   ├── google.png
    │   │   │   │   ├── kaixin001.png
    │   │   │   │   ├── msn.png
    │   │   │   │   ├── qq.png
    │   │   │   │   ├── qq2.png
    │   │   │   │   ├── qzone.png
    │   │   │   │   ├── rr.png
    │   │   │   │   ├── sina.png
    │   │   │   │   ├── sohu.png
    │   │   │   │   └── tianya.png
    │   │   │   ├── share.xml
    │   │   │   └── style.swf
    │   │   ├── errorCode.json
    │   │   ├── ezuikit
    │   │   │   ├── ezuikit-talk.js
    │   │   │   └── ezuikit.js
    │   │   ├── flv.min.js
    │   │   ├── hls.js
    │   │   ├── hls.js.map
    │   │   ├── hls.min.js
    │   │   ├── jquery.min.js
    │   │   ├── jsPlugin-1.2.0.js
    │   │   ├── jsPlugin-1.2.0.min.js
    │   │   ├── jsPlugin-1.2.0_test.js
    │   │   ├── jsmpeg.min.js
    │   │   ├── layer
    │   │   │   ├── layer.js
    │   │   │   └── theme
    │   │   │       └── default
    │   │   │           ├── icon-ext.png
    │   │   │           ├── icon.png
    │   │   │           ├── layer.css
    │   │   │           ├── loading-0.gif
    │   │   │           ├── loading-1.gif
    │   │   │           └── loading-2.gif
    │   │   ├── playctrl
    │   │   │   ├── AudioRenderer.js
    │   │   │   ├── DecodeWorker.js
    │   │   │   ├── Decoder.js
    │   │   │   ├── Decoder.wasm
    │   │   │   ├── SuperRender_10.js
    │   │   │   └── SuperRender_20.js
    │   │   ├── talk
    │   │   │   ├── adapeter.js
    │   │   │   ├── janus.js
    │   │   │   ├── recoder.js
    │   │   │   ├── recorder.js
    │   │   │   └── tts.js
    │   │   ├── transform
    │   │   │   ├── SystemTransform.js
    │   │   │   ├── SystemTransform.js.mem
    │   │   │   └── systemTransform-worker.min.js
    │   │   ├── wav-audio-encoder.js
    │   │   └── worker.js
    │   ├── readme.txt
    │   └── tabs_dynamic.html
    └── ros_20201209.tgz

121 directories, 373 files