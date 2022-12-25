> [RLP-VIO: Robust and lightweight plane-based visual-inertial odometry for augmented reality](https://onlinelibrary.wiley.com/doi/10.1002/cav.2046)  
> [Jinyu Li](https://github.com/itsuhane), [Xin Zhou](https://github.com/ZhouXiner), [Bangbang Yang](https://github.com/ybbbbt), [Guofeng Zhang*](https://github.com/guofengzhang), Xun Wang ,and Hujun Bao   
> CAVW 2022, pp. e2046, 2022.   

## How to use

For compilation:

* Install the dependencies: Eigen, Ceres Solver and OpenCV.

* Clone the repository.

* Build with 

  ```shell
  mkdir -p build && cd build && cmake -DCMAKE_BUILD_TYPE=Release  .. && make -j8
  ```

  > you will need a compiler supporting C++17.

* Tested in Ubuntu 18.04 (with GCC 9.0 and CMake 3.11), and macOS 10.14.

For execution:
* `path/to/pvio-pc [data_scheme]://[data_path] [config_yaml_path] [result.tum]`
  * e.g.
    * For EuRoC Dataset: `build/pvio-pc/pvio-pc euroc:///Data/EuRoC/V1_01_easy/mav0 config/euroc.yaml result/trajectory.tum`
    * For TUM-VI Dataset: `build/pvio-pc/pvio-pc tum:///Data/TUM_VI/dataset-room1_512_16/mav0 config/tum_vi.yaml result/trajectory.tum`
* The trajectory will be written in `trajectory.tum`.

## Publication

If you use this source code for your academic publication, please cite the following paper.
```
@article{li2022rlp,
  title={RLP-VIO: Robust and lightweight plane-based visual-inertial odometry for augmented reality},
  author={Li, Jinyu and Zhou, Xin and Yang, Bangbang and Zhang, Guofeng and Wang, Xun and Bao, Hujun},
  journal={Computer Animation and Virtual Worlds},
  pages={e2046},
  year={2022},
  publisher={Wiley Online Library}
}
```

## Acknowledgements

This work is affliated with ZJU-SenseTime Joint Lab of 3D Vision, and its intellectual property belongs to SenseTime Group Ltd.

## Copyright
```
Copyright (c) ZJU-SenseTime Joint Lab of 3D Vision. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
