
# VEDAI

[VEDAI](https://downloads.greyc.fr/vedai/) dataset prepared for [darknet](https://github.com/AlexeyAB/darknet) implementation

All images converted to `.jpg`  
All annotations are standartized to `<object-class> <x> <y> <width> <height>`, where:  

* `<object-class>` - integer number of object from 0 to (classes-1)  
* `<x> <y> <width> <height>` - float values relative to width and height of image, it can be equal from 0.0 to 1.0  
* for example: `<x> = <absolute_x> / <image_width> or <height> = <absolute_height> / <image_height>`  
* atention: `<x> <y>` - are center of rectangle (are not top-left corner)  

## Classes:  

0 - car  
1 - truck  
2 - pickup  
3 - tractor  
4 - camping car  
5 - boat  
6 - motorcycle  
7 - bus  
8 - van  
9 - other  
10 - small  
11 - large  


## List of excluded images  
You can find it in /unmarked/

00000024.jpg  
00000039.jpg  
00000522.jpg  
00000606.jpg  
00000887.jpg  
00001185.jpg  
00000028.jpg  
00000424.jpg  
00000560.jpg  
00000717.jpg  
00001143.jpg  
00001244.jpg  
00000034.jpg  
00000425.jpg  
00000600.jpg  
00000878.jpg  
00001145.jpg  
00001248.jpg

The weight of YOLO_v2 airborne detection:
https://www.dropbox.com/s/oo2uis4442by3f1/yolov2-vedai_UCAS_final.weights?dl=0

./darknet detect cfg/yolov2-vedai.cfg yolov2-vedai_UCAS_final.weights data/train/unmarked/00000024.jpg

![detection](experimental_result/predictions_028.jpg)
![detection](experimental_result/predictions_024.jpg)
![detection](experimental_result/predictions_034.jpg)
![detection](experimental_result/predictions_878.jpg)

after execution of the above statement we get the results in the darknet folder itself.
