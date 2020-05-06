# Computational Data Pipelines with 

Learn about PyTorch:
* Paszke, A., Gross, S., Massa, F., Lerer, A., Bradbury, J., Chanan, G., Killeen, T., Lin, Z., Gimelshein, N., Antiga, L. and Desmaison, A., 2019. PyTorch: An imperative style, high-performance deep learning library. In Advances in Neural Information Processing Systems (pp. 8024-8035). [pdf](https://papers.nips.cc/paper/9015-pytorch-an-imperative-style-high-performance-deep-learning-library.pdf)
* PyTorch Tutorials https://pytorch.org/tutorials/

Learn about using deep learning for *image style transfer*: 
* Gatys, L.A., Ecker, A.S. and Bethge, M., 2016. Image style transfer using convolutional neural networks. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 2414-2423). [pdf](http://openaccess.thecvf.com/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf)
* Image Style Transfer with Open CV https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/


# Challenge 

1. Fork https://github.com/MSDS-6311/uh-demo in your github account and clone it on your instance. 
2. Run `StyleTransfer.ipynb`
3. Create a new notebook designing a new datajoint schema that catalogs something (e.g. famous people, fine art, your own photos), then downloads photos from URLs, applies style transfers, and plots a selection of results.

Note: you will need to install `cv2` using the command (on Ubuntu): 
```shell
$ sudo apt install python3-opencv
$ sudo pip3 install opencv-contrib-python
```
