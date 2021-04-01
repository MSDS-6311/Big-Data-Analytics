 Computational Data Pipelines

What is workflow management? 
* Common Workflow Language: [https://www.youtube.com/watch?v=86eY8xs-Vo8]
* Signac: [https://www.youtube.com/watch?v=CCKQH1M2uR4]
* DataJoint: [https://www.youtube.com/watch?v=rllclTIeI5Q]


Learn about using deep learning for *image style transfer*:
* Gatys, L.A., Ecker, A.S. and Bethge, M., 2016. Image style transfer using convolutional neural networks. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 2414-2423). [pdf](http://openaccess.thecvf.com/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf)
* Image Style Transfer with Open CV https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/
* A simple example https://www.kaggle.com/bhallaakshit/neural-style-transfer-with-opencv/notebook

Note: you will need to install `cv2` and `graphviz` using the command (on Ubuntu):
```shell
$ sudo apt install python3-opencv
$ sudo pip3 install opencv-contrib-python
$ sudo apt install graphviz 
```

## 

## Launch MySQL database server using 

On your own EC2 instance, clone datajoint
```shell
$ git clone https://github.com/datajoint/datajoint-python
```

Install DataJoint for Python
```sh
$ cd datajoint-python
$ pip install -e .
```


Create an `.env` with desired development environment values e.g.

```sh
PY_VER=3.7
ALPINE_VER=3.10
MYSQL_VER=5.7
MINIO_VER=RELEASE.2019-09-26T19-42-35Z
UID=1000
GID=1000
```

Then copy the `docker-compose.yml` file and start the database service

```sh
$ cp local-docker-compose.yml docker-compose.yml
$ sudo docker-compose up -d
```
The `root` password in the database server is `simple`


## Build computational pipelines 
1. Fork https://github.com/MSDS-6311/StyleTransfer in your github account and clone it on your instance. 
2. In notebooks Run `States.ipynb`
3. Add a new computed table, `StateHSV` computing the average hue, saturation, and value of the flags.
4. Plot the US States flags ordered by hue.

## Submitting the homework 
Submit your work by committing it in your repository and pushing it to your github repo.
