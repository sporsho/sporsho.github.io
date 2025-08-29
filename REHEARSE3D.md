# REHEARSE-3D: A Multi-modal Emulated Rain Dataset for 3D Point Cloud De-raining

### Authors: Abu Mohammed Raisuddin<sup>1</sup>, Jesper Holmblad<sup>1</sup>,  Hamed Haghighi<sup>2</sup>, Yuri Poledna<sup>3</sup>,  Maikol Funk Drechsler<sup>3</sup>, Valentina Donzella<sup>2</sup> and Eren Erdal Aksoy<sup>1</sup>

### Affiliations
1. Halmstad University 
2. University of Warwick 
3. Technische Hochschule Ingolstadt

## Data Download 
[Click Here to Download REHEARSE3D](https://s3.ice.ri.se/roadview-rehearse3d_public/REHEARSE3D_PUBLIC.zip)


Simulated Data Link Coming Soon


The data directory structure is shown below. The root folder name is ```REHEARSE3D_PUBLIC```. Following the Semantic Kitti structure, there is ```sequences``` folder inside the root folder. 
Inside it, there are 143 sequences numbered from ```000``` to ```142```. 
Each numbered sequence contains data from multiple sensors for about 30 seconds. 
Inside the numbered folder (e.g., ```000``` ) there are 9 sub-folders (```arena```, ```ext_radar```, 
```flir```, ```innoviz```, ```ouster``` , ```radar_pcd```, ```weather```, ```lidar_radar_pcd```, 
and ```lidar_radar_labels```). 
* ```arena``` contains RGB data 
* ```ext_radar``` contains extended radar data, along with the 3d coordinates, this folder contains the intensity, cross section, velocity, and confidence data. 
* ```flir``` contains thermal camera images 
* ```innoviz``` contains 3d point clouds form innoviz lidar sensor. 
* ```ouster``` contains 3d point clouds from ouster lidar sensor. 
* ```radar_pcd``` contains 3d point cloud from radar. 
* ```weather``` contains weather data (e.g., device temperature, dew point, humidity, luminosity, pressure, relative humidity, wind direction, wind speed, etc. )
* ```lidar_radar_pcd``` contains merged innoviz and radar point clouds. 
* ```lidar_radar_pcd``` contains the labels of merged innoviz and radar point cloud. 
```
REHEARSE3D_PUBLIC
|
|- sequences 
    |
    |- 000 
        |
        |- arena 
            |- 000000.jpeg 
            .
            .
            .
            |- 000297.jpeg 
            |- metadata.csv 
        |
        |- ext_radar 
            |- 000000.csv 
            .
            .
            .
            |- 000495.csv 
            |- metadata.csv 
        |
        |- flir 
            |- 000000.jpeg 
            .
            .
            .
            |- 000297.jpeg 
            |- metadata.csv 
        |
        |- innoviz
            |- 000000.bin
            .
            .
            .
            |- 000293.bin 
            |- metadata.csv 
        |
        |- ouster
            |- 000000.bin
            .
            .
            .
            |- 000297.bin 
            |- metadata.csv 
        |
        |- radar_pcd
            |- 000000.bin
            .
            .
            .
            |- 000495.bin 
            |- metadata.csv 
        |
        |- weather 
            |- 000000.csv 
            .
            .
            .
            |- 000029.csv 
        |
        |- lidar_radar_pcd 
            |- 000000.bin
            .
            .
            .
            |- 000293.bin 
        |- lidar_radar_labels
            |- 000000.label
            .
            .
            .
            |- 000293.label 
        
    |
    |- 001 
    .
    .
    .
    |- 142
```


## Saved Model

[Outdet Weights](REHEARSE3D/outdet/outdet.pt)


[SalsaNext Weights](https://s3.ice.ri.se/roadview-rehearse3d_public/salsanext/SalsaNext_valid_best)

## Hyperparameters
Will be available soon. 

## Rain Removal with 3D-OutDet and SalsaNext
[![Rain Removal on REHEARSE-3D](https://img.youtube.com/vi/HnQxf5jjvsI/0.jpg)](https://www.youtube.com/watch?v=HnQxf5jjvsI)

# Acknowledgement 
We thank Foxglove Technologies, Inc. for publishing a very nice tutorial on REHEARSE-3D dataset. The Tutorial can be found [here](https://foxglove.dev/blog/working-with-scenes-and-pointclouds?utm_content=344639551&utm_medium=social&utm_source=twitter&hss_channel=tw-1356767330856955904)
