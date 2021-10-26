# AVoE: A Synthetic 3D Dataset on Understanding Violation of Expectation for Artificial Cognition
![111](https://user-images.githubusercontent.com/51585075/138597425-6bc359e9-92ff-48f2-a1dc-ef1bffa143ed.JPG)


# Paper

[[ArXiv]](https://arxiv.org/abs/2110.05836) 


## AVoE Dataset
Download the respective dataset along with the annotation from here: 

[[Dataset]](https://drive.google.com/drive/folders/1cUzuR-lhfOgXUz6zhNIIAYqj4mLu7qCN?usp=sharing)


You may download down and put it into your own drive,then you can `gdown <Drive Url to upload to server>` 

## Dataset Structure
The dataset consists of five violations of expectation event categories:
A. Support
B. Occulsion
C. Containment
D. Collision
E. Barrier

There are 500 trials in each event category (75% Train, 15% Val, 10% Test). The `train` folder contains only expected videos while the `validation` and `test` folders contain both expected and surprising videos. Surprising and expected videos with the same stimuli have the same trial ID.

Each trial folder has an `rgb.avi` which is the RGB video. The folder also has a `physical_data.json` which contains the ground truth values of features, prior rules and posterior rules. There is also a `scene_data.json` which has frame-by-frame values of the position and rotation of all entities (object, occluder, barrier, support, container) along with the instance IDs of all entities.

Use `utils.py` to generate frames and videos of the depth and instance segmented images from `depth_raw.npz` and `inst_raw.npz` located in every trial folder. Do edit the settings section of `utils.py` to your needs.

## Dataset Generation System Requirements
- Blender 2.83 with eevee engine
- **Python 3.6**



## If you use AVoE, please cite the our paper:


    @article{dasgupta2021avoe,
      title={AVoE: A Synthetic 3D Dataset on Understanding Violation of Expectation for Artificial Cognition},
      author={Dasgupta, Arijit and Duan, Jiafei and Ang Jr, Marcelo H and Tan, Cheston},
      journal={arXiv preprint arXiv:2110.05836},
      year={2021}
    }




