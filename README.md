# HFR Dataset

Dataset proposed in "ARVo: Learning All-Range Volumetric Correspondence for Video Deblurring", CVPR 2020.


### Download
https://drive.google.com/drive/folders/1F7sC6vWXiJ3HQDMCJw8Wa2tqulaSLfC-?usp=sharing

### Folder Format

```
hfr/
├── train/
|   ├── C1113  (Video1)
|   │   ├── blurry_resize (input blurred video frames)
|   │   │   ├── C1113_frame00020.png
|   │   │   ├── C1113_frame00061.png
|   │   │   ├── C1113_frame00102.png
|   │   │   ├── ...
|   │   │   
|   │   ├── sharp_resize (target unblurred video frames)
|   │       ├── C1113_frame00020.png
|   │       ├── C1113_frame00061.png
|   │       ├── C1113_frame00102.png
|   │       ├── ...
|   │   
|   ├── C1114  (Video2)
|   ├── ...    (Videos)
|
├── test/
|
```

The frame ids are not continuous, but numerically sorted, i.e., one can get the correct frame sequence by sorting these frame images by their names.

Be sure to check beforehand because some existing code bases assummed a different folder format, where blur/gt is at higher folder level to the videos.

```
|--dataset  
    |--blur  
        |--video 1
            |--frame 1
            |--frame 2
                ：  
        |--video 2
            :
        |--video n
    |--gt
        |--video 1
            |--frame 1
            |--frame 2
                ：  
        |--video 2
        	:
        |--video n
```
