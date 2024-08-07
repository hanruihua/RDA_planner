<!-- | **[`PDF_IEEE`](https://ieeexplore.ieee.org/document/10036019)** | **[`PDF_Arxiv`](https://arxiv.org/pdf/2210.00192.pdf)** | **[`Video_Youtube`](https://www.youtube.com/watch?v=qUNMQQRhNFo)** | **[`Video_Bilibili`](https://www.bilibili.com/video/BV1zT411d7aL/?vd_source=cf6ba629063343717a192a5be9fe8985)** |  -->
<div align="center">

 # RDA Planner

<a href="https://ieeexplore.ieee.org/document/10036019"><img src='https://img.shields.io/badge/PDF-IEEE-brightgreen' alt='PDF'></a>
<a href="https://arxiv.org/pdf/2210.00192.pdf"><img src='https://img.shields.io/badge/ArXiv-2210.00192-brightgreen' alt='ArXiv'></a>
<a href="https://github.com/hanruihua/RDA_planner/releases"><img src='https://img.shields.io/github/v/release/hanruihua/RDA_planner?color=orange' alt='version'></a>
<a href="https://www.youtube.com/watch?v=qUNMQQRhNFo"><img src='https://img.shields.io/badge/Video-Youtube-blue' alt='youtube'></a>
<a href="https://www.bilibili.com/video/BV1zT411d7aL/?vd_source=cf6ba629063343717a192a5be9fe8985"><img src='https://img.shields.io/badge/Video-Bilibili-blue' alt='bilibili'></a>
<a href="#citation"><img src='https://img.shields.io/badge/BibTex-RDA_planner-lightgreen' alt='Paper BibTex'></a>
<a href="https://github.com/hanruihua/RDA_planner/blob/main/LICENSE"><img src='https://img.shields.io/badge/License-MIT-yellow' alt='Paper BibTex'></a>



</div>

RDA planner is a fast and efficient motion planner for autonomous navigation in cluttered environments. The key idea of RDA is to decompose the complex optimization problem into several subproblems by ADMM, which allows the collision avoidance constraints to be computed in parallel for each obstacle to reduce computation time significantly. 

Features:
  - Shape aware planner, which can tackle robots and obstacles with arbitrary convex shapes.
  - Highly accurate control achieved through the use of an optimization solver. 
  - Support for both static and dynamic obstacles
  - Fast computation time, which is suitable for real-time applications.
  - Support different types of dynamics, including differential, Ackermann, and omnidirectional robots.


## Prerequisite
- Python >= 3.7

## Installation 

```
git clone https://github.com/hanruihua/RDA_planner
cd RDA_planner
pip install -e .  
```

## Run examples

**Path Track (example/path_track.py)**                 |  <img src="example\path_track\animation\path_track.gif" width="400" />  
|:-------------------------:|:-------------------------:|
**Cross Corridor (example/corridor.py)** | <img src="example\corridor\animation\corridor.gif" width="500" />|
**Reverse Parking (example/reverse.py)** | <img src="example\reverse\animation\reverse_park.gif" width="400" />
**Input Lidar points (example/lidar_path_track.py)** | <img src="example\lidar_nav\animation\path_track.gif" width="400" />


**Dynamic obstacles avoidance (example/dynamic_obs.py)** | <img src="example\dynamic_obs\animation\dynamic_obs1.gif" width="300" /> |  <img src="example\dynamic_obs\animation\dynamic_obs2.gif" width="300" />
|:-------------------------:|:-------------------------:|:-------------------------:|

**Note:** You can customize the scenario by modifying the parameters in the corresponding yaml file as introduced in [ir_sim](https://github.com/hanruihua/ir_sim). For the polygon obstacles, please make sure the obstacles are convex (CCW order is not necessary now).


## Citation

If you find this code or paper is helpful, you can **star** this repository and cite our paper by the following **BibTeX** entry:

```
  @ARTICLE{10036019,
  author={Han, Ruihua and Wang, Shuai and Wang, Shuaijun and Zhang, Zeqing and Zhang, Qianru and Eldar, Yonina C. and Hao, Qi and Pan, Jia},
  journal={IEEE Robotics and Automation Letters}, 
  title={RDA: An Accelerated Collision Free Motion Planner for Autonomous Navigation in Cluttered Environments}, 
  year={2023},
  volume={8},
  number={3},
  pages={1715-1722},
  doi={10.1109/LRA.2023.3242138}}

```
