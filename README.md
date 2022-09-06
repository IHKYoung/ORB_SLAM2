# Fixed ORB_SLAM2 for Ubuntu20 and later
## 解决的问题
安装ORB-SLAM2的问题：

1. 需要使用C++14以上的标准

2. 需要debug部分源码

   1. ```cpp
      # include/LoopClosing.h
      Eigen::aligned_allocator<std::pair<KeyFrame* const, g2o::Sim3> > > KeyFrameAndPose;
      ```

   2. `add #include <unistd.h> in System.h`

3. 解决Eigen的问题

   就是不需要自带的cmake_modules，然后软链接一个Eigen


