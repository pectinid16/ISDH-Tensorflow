# ISDH-Tensorflow
Implemement of Instance Similarity Deep Hashing for Multi-Label Image Retrieval

### Requirements
- [Linux](https://www.ubuntu.com/download)
- [Tensorflow](https://www.tensorflow.org/)
- [NVIDIA GPU + CUDA CuDNN](https://developer.nvidia.com/cudnn)

### Getting Started:
- Prepare the datasets  
Download the [flickr dataset](http://press.liacs.nl/mirflickr/) and put the images into folder  `/data/flickr/images/`
  
- Transform the train images in tfrecord format  
Run `python tf_record.py`, and `train-flickr.tfrecords` will be generated
         
- Prepare the AlexNet weights trained on ImageNet  
Download from [here](ww.cs.toronto.edu/~guerzhoy/tf_alexnet/bvlc_alexnet.npy) and put it on current directory
   
- Train:  
Run `sh train-flickr.sh`, and the trained model will be saved in `models/ISDH-48b/`.

- Test:  
Run `sh test-flickr.sh`, and generated hash codes will be saved in `./results/ISDH_48b_test_flickr.txt`.


### Other Datasets:
- [NUS-WIDE](http://lms.comp.nus.edu.sg/research/NUS-WIDE.htm)
- [VOC2012](http://cvlab.postech.ac.kr/~mooyeol/pascal_voc_2012/)

### Acknowledgement
- [Tensorflow Implementation of AlexNet](https://kratzert.github.io/2017/02/24/finetuning-alexnet-with-tensorflow.html)    
    
