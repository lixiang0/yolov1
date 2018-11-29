# Pedestrian-Detection by YOLOv1 in PyTorch


<p align="center">
  <img src="/2.png" alt="Pedestrian Detector in action"></img>
</p>


## Dataset
The [TownCentre](http://www.robots.ox.ac.uk/ActiveVision/Research/Projects/2009bbenfold_headpose/project.html#datasets) dataset is used for training our pedestrian detector. You can use the following commands to download the dataset. This automatically extracts the frames from the video, and creates XML files from the csv groundtruth. The image dimensions are downscaled by a factor of 2 to reduce processing overhead.
```
wget http://www.robots.ox.ac.uk/ActiveVision/Research/Projects/2009bbenfold_headpose/Datasets/TownCentreXVID.avi
wget http://www.robots.ox.ac.uk/ActiveVision/Research/Projects/2009bbenfold_headpose/Datasets/TownCentre-groundtruth.top
mv TownCentreXVID.avi test.avi
python xx_extract_imgs.py
python xx_extract_xml.py
python xx_generate_xml2txt.py
```

**Train**
```
python train.py
```

**Test for files**
```
python test_file.py
```


**Test for video**
```
python test_video.py
```

