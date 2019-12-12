# DPC-Captions

This is an open-source image captions dataset for the aesthetic evaluation of images, which we completed in the [Victory team of Besti](https://www.victory-lab.net/).

It is a new dataset named DPC-Captions, which contains comments of up to five aesthetic attributes of one image through knowledge transfer from a full-annotated small-scale dataset. Then, we propose Aesthetic Multi-Attribute Network (AMAN), which is trained on a mixture of fully-annotated small-scale PCCD dataset and weakly-annotated large-scale DPC-Captions dataset. Our AMAN makes full use of transfer learning and attention model in a single framework. The experimental results on our DPC-Captions and PCCD dataset reveal that our method can predict captions of five aesthetic attributes together with numerical score assessment of each attribute. We use the evaluation criteria used in image captions to prove that our specially designed AMAN model outperforms traditional CNN-LSTM model and modern SCA-CNN model of image captions.

### DPC-Captions Dataset via Knowledge Transfer

The aesthetic attributes of image captions are from PCCD[1], which contains comments and a score for each of the 7 aesthetic attributes (including overall impression, etc.). However, the scale of PCCD is quite small (only 4235 images). While the AVA[2] dataset contains 255,530 images with an assessment score distribution for each image. The images and score distributions of AVA dataset are crawled from the website of DPChallenge.com. Their exist comments from multiple reviewers attached for every image. However, the multiple comments are not arranged by aesthetic attributes. We then crawl 330,000 images together with their comments from DPChallenge.com. We call this dataset AVA-Plus.    
Images of DPC-Captions are selected from the AVA-Plus with the help of PCCD datasets. The aesthetic attributes of PCCD dataset include ***Color Lighting***, ***Composition***, ***Depth of Field***, ***Focus***, ***General Impression*** and ***Use of Camera***. For each aesthetic attribute, keywords of top 5 frequency are selected from the captions. We omit the adverbs, prepositions and conjunctions. We combine words with similar meaning such as color and colour, colors and colors. A statistic of the keywords frequency are shown in the table below.

[1] Chang K Y, Lu K H, Chen C S. Aesthetic critiques generation for photos[C]//Proceedings of the IEEE International Conference on Computer Vision (ICCV). 2017: 3514-3523.

[2] Murray N, Marchesotti L, Perronnin F. AVA: A large-scale database for aesthetic visual analysis[C]//2012 IEEE Conference on Computer Vision and Pattern Recognition (CVPR). IEEE, 2012: 2408-2415.

*************************************************************************************
### Aesthetic Attribute Keywords and Frequency of PCCD Dataset.

| Aesthetics Attributes      | Top 5 Keywords (Frequency)     |
| ---------- | :-----------:  |
| Color Lighting     | lighting (5829), color (5637), light (1708), sky (493), shadows (491)     |
| Composition     | composition (13749), left (2691), perspective (1787), shot (1715), lines (1369)     |
| Depth of Field     | depth (6087), field (5822), focus (1098), background (952), aperture (550)     |
| Focus     | focus (7537), sharp (1308), eyes (402), see (345), camera (337)     |
| General Impression     | impression (4401), general (4357), good (1810), great (1338), nice (1040)     |
| Subject of Photo     | subject (6594), interesting (708), beautiful (386), light (209), capture (200)     |
| Use of Camera     | exposure (1619), speed (1488), shutter (1113), iso (1049), aperture (665)     |
  
### The Knowledge Transfer Method From PCCD to Our DPC-Captions
   
![](https://i.loli.net/2019/12/12/t9Fq7QGh5e8sTbE.png)  

  
**PS: Considering the copyright of images, we will only open-source the picture number public.**
  
### Our Paper  
  
Xin Jin, Le Wu, Geng Zhao, Xiaodong Li, Xiaokun Zhang, Shiming Ge, Dongqing Zou, Bin Zhou, Xinghui Zhou. Aesthetic Attributes Assessment of Images. ACM Multimedia (ACMMM), Nice, France, 21-25 Oct. 2019. **[pdf-HD](http://jinxin.me/downloads/papers/031-MM2019/MM2019-HighRes.pdf)**(31.1MB)  **[pdf-LR](http://jinxin.me/downloads/papers/031-MM2019/MM2019-LowRes.pdf)**(1.11MB) **[arXiv](https://arxiv.org/abs/1907.04983)**(1907.04983)


### Citation

Please cite the ACM Multimedia paper if you use DPC-Captions in your work:

```
@inproceedings{DBLP:conf/mm/JinWZLZGZZZ19,
  author    = {Xin Jin, Le Wu, Geng Zhao, Xiaodong Li, Xiaokun Zhang, Shiming Ge, Dongqing Zou, Bin Zhou and Xinghui Zhou},
  title     = {Aesthetic Attributes Assessment of Images},
  booktitle = {Proceedings of the 27th {ACM} International Conference on Multimedia,
               {MM} 2019, Nice, France, October 21-25, 2019},
  pages     = {311--319},
  year      = {2019},
  crossref  = {DBLP:conf/mm/2019},
  url       = {https://doi.org/10.1145/3343031.3350970},
  doi       = {10.1145/3343031.3350970},
  timestamp = {Fri, 06 Dec 2019 16:44:03 +0100},
  biburl    = {https://dblp.org/rec/bib/conf/mm/JinWZLZGZZZ19},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```
