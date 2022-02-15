# An-Intelligent-Hybrid-Text-To-Image-Synthesis-Model-for-Generating-Realistic-Human-Faces
This project page provides pytorch code that implements the following paper:

Title: "An Intelligent Hybrid Text-To-Image Synthesis Model for Generating Realistic Human Faces"

Link: https://ieeexplore.ieee.org/document/9694194

### How to use
#### Python
*	Python2.7
*  Pytorch0.4 (conda install pytorch=0.4.1 cuda90 torchvision=0.2.1 -c pytorch)
*  tensorflow (pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp27-none-linux_x86_64.whl)
*  pip install easydict pathlib
*  conda install requests nltk pandas scikit-image pyyaml cudatoolkit=9.0
	
#### Data
* Download [metadata for faces](https://drive.google.com/file/d/16m-eR9W8dm0-T21igA1dwVq0fAZwnnGX/view?usp=sharing) and extract them to data/faces/
	*	python google_drive.py 1ao16xGvVmBltWadn21fIpxk2NGytEBLg ../data/faces.zip	

#### Pretrained Models
* [DAMSM for faces](https://drive.google.com/file/d/1ibwy7-sZ2xVi5Qp_hZsic1TjmIjRmMwX/view?usp=sharing) : Download and extract it to DAMSMencoders/
    * python google_drive.py 1ao16xGvVmBltWadn21fIpxk2NGytEBLg DAMSMencoders/faces.zip

#### Training
	1- go into code/folder
	2- python main.py --cfg cfg/faces_DMGAN.yml --gpu 0

#### Validation
	1- Image Generation
		1- go into code/ folder
		2- python main.py --cfg cfg/eval_faces.yml --gpu 0
