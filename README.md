# Graph Convolutional Networks for Hyperspectral Image Classification

[Danfeng Hong](https://sites.google.com/view/danfeng-hong), [Lianru Gao](https://scholar.google.com/citations?user=f6OnhtcAAAAJ&hl=zh-CN), [Jing Yao](https://scholar.google.com/citations?user=1SHd5ygAAAAJ&hl=en), [Bing Zhang](http://english.radi.cas.cn/Education/PhDS/201401/t20140109_115415.html), [Antonio Plaza](https://www.umbc.edu/rssipl/people/aplaza/), [Jocelyn Chanussot](http://jocelyn-chanussot.net/)
---------------------

The code in this toolbox implements the ["Graph Convolutional Networks for Hyperspectral Image Classification"](https://ieeexplore.ieee.org/document/9170817).
More specifically, it is detailed as follow.

![alt text](./Motivation_GCN.png)

Citation
---------------------

**Please kindly cite the papers if this code is useful and helpful for your research.**

D. Hong, L. Gao, J. Yao, B. Zhang, A. Plaza, J. Chanussot. Graph Convolutional Networks for Hyperspectral Image Classification, IEEE Trans. Geosci. Remote Sens., 2020, DOI: 10.1109/TGRS.2020.3015157. 

     @article{hong2020graph,
      title     = {Graph Convolutional Networks for Hyperspectral Image Classification},
      author    = {D. Hong and L. Gao and J. Yao and B. Zhang and A. Plaza and J. Chanussot},
      journal   = {IEEE Trans. Geosci. Remote Sens.}, 
      year      = {2020},
      note      = {DOI:10.1109/TGRS.2020.3015157}
      publisher = {IEEE}
     }


System-specific notes
---------------------
The data were generated by Matlab R2016a or higher versions, and the codes of various networks were tested in Tensorflow in Python 3.7 on Windows 10 machines.

How to use it?
---------------------

Here an example experiment is given by using Indian Pine data. Directly run .py functions with different networks to reproduce the results on the Indian Pine data, which exists in the aforementioned paper. Please note that we fixed the randomness of the parameter initialization to reproduce the unchanged results.

This toolbox consists of eight hyperspectral classification networks as follows

1DCNN: one-dimensional convolutional neural network  
2DCNN: two-dimensional convolutional neural network  
3DCNN：three-dimensional convolutional neural network, which can be found from the paper (Deep Feature Extraction and Classification of Hyperspectral Images Based on Convolutional Neural Networks, Chen et al., TGRS 2016)  
GCN: graph convolutional network  
miniGCN: mini-batch GCN  
FuNet-A: fusion networks with additive fusion  
FuNet-M: fusion networks with element-wise multiplicative fusion  
FuNet-C: fusion networks with concatenation fusion  

If you want to run the code in your own data, you have to 

first of all, use the matlab functions in the folder of DataGenerate_Funciton to prepare the network input data;  
next, change the save route or directly copy the generated data into the folder of HSI_CNN or HSI_GCN;  
finally, run the .py networks.

Moreover, we provide the fucntion of draw_ClassificaitonMap.m to draw the classification maps with the given colormap function, i.e., giveColorCM_HH.m.

If you encounter the bugs while using this code, please do not hesitate to contact us.

:exclamation: The variable in `X_test.mat` was converted to single-precision for efficient use of memory, which may cause slight admissible perturbation on actual results. Due to its large size, you may need to manually download `X_test.mat` to your local in the folder under path `IEEE_TGRS_GCN/HSI_CNN/` by the given the links of google drive or baiduyun as follows

Google drive: https://drive.google.com/file/d/1JonHPynVZWCQ9EvZA-oXiFEPU-giIaYt/view?usp=sharing

Baiduyun: https://pan.baidu.com/s/1XRcKsckcYTqnD_zjOvWHoQ (access code: mrdf)

Licensing
---------

Copyright (C) 2020 Danfeng Hong

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3 of the License.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.

Contact Information:
--------------------

Danfeng Hong: hongdanfeng1989@gmail.com<br>
Danfeng Hong is with the Univ. Grenoble Alpes, CNRS, Grenoble INP, GIPSA-lab, 38000 Grenoble, France.

