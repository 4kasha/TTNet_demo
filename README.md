[//]: # (Image References)

[image1]: media/test1_result.gif "Result1"
[image2]: media/test2_result.gif "Result2"
[image3]: media/test2_invert.gif "Result_inv"

# TTNet Demo

## Details 

* [OpenTTGames Dataset](https://lab.osai.ai/datasets/openttgames/) (Full-HD videos, **120** fps)
* Multi-Task : Ball detection, Semantic segmentation, Events spotting
    * Ball size : about **15** pixels on average (color : Magenta) 
    * Segmentation : humans(G), table(B) and scoreboard(R) classes with channel-wise encoding
    * Events : "bounce" and "over net"
* Input : downscaled video frames (320px,128px) and **9** frame sequences (less than 0.1s in real time)
* Annotation : Event - center frame, Ball position and seg mask - last frame, respectively
* Inference capability : more than 166 fps on a machine with a single NVIDIA RTX 2080Ti GPU


A demo (60 fps) by a trained model (loss condition : Unbalanced) using following repository: https://github.com/maudzung/TTNet-Real-time-Analysis-System-for-Table-Tennis-Pytorch

|       test_1.mp4    |      test_2.mp4     |
|:-------------------:|:-------------------:|
|![Result1][image1]|![Result2][image2]|

This model is almost robust for time invertion input.

![Result_inv][image3]

## Application to videos from YouTube




## Reference

* [R Voeikov, et al. "TTNet: Real-time temporal and spatial video analysis of table tennis" (CVPR 2020)](https://arxiv.org/pdf/2004.09927.pdf), [YouTube](https://www.youtube.com/watch?v=WrEYIXrHkL8)
* [A Kendall, et al. "Multi-task learning using uncertainty to weigh losses for scene geometry and semantics" (CVPR 2018)](https://arxiv.org/pdf/1705.07115.pdf), [Supplementary](https://github.com/Hui-Li/multi-task-learning-example-PyTorch)