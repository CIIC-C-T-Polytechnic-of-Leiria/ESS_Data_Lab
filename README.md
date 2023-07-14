## Burned area semantic segmentation: a novel dataset and evaluation using convolutional networks

---

<p align="center">
<img src="assets/CIIC_logo.png" width="1000px"/>
</p>

---
<div align="center">

 [Paper](https://www.sciencedirect.com/science/article/pii/S0924271623001831) | [Dataset](https://zenodo.org/record/7944963#.ZGYoxHbMIQ8) | [Paper Citation](#article-citation) |  [Dataset Citation](#dataset-citation)

</div>

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FCIIC-C-T-Polytechnic-of-Leiria%2FESS_Data_Lab&countColor=%23263759&style=plastic)

### Description

Wildfires have significant impacts on the environment, society, and economy, therefore understanding the dynamics of wildfires is crucial to evaluate such effects. Nevertheless, monitoring and measuring the burned area by traditional, non-automatic methods remains time-consuming and challenging. 

For several years, automatic semantic segmentation models have been used to describe natural phenomena, but deep learning models have recently achieved very competitive results. However, this new breed of models typically needs annotated datasets of significant dimensions. Nonetheless, datasets for real-time burnt area segmentation are often scarce.

We propose a new manually annotated dataset for segmentation of forest fire burned area based on a video captured by a UAV to train and evaluate semantic segmentation models. We explore deep learning-based techniques and establish baselines. We also suggest specific temporal consistency metrics to validate burned area polygons generated by the models. By applying U-Net network models, we obtain IoU values superior to 95\% on the test set and competitive temporal consistency compared to classical machine learning approaches in the successive frames generated by the model based on non-annotated data.

### Dataset Description

The dataset consists of a total of 249 frames and corresponding segmentation masks. The subset considered for training and validation contains 226 frame-mask pairs approximately 90% while the test subset contains 23 pairs approximately 10%.

<p align="center">
<img src="assets/Freq_Segmentacao_v3.png" width="1000px"/> 
</p>

Each of the training and validation frames was generated by taking a sample every 4 seconds (corresponds to 100 frames) starting at the initial one and ending at frame 22500. The frames and annotations of the test set have the same sampling rate but are offset from the 50 frames (2 seconds) of the training and validation frames to avoid overlapping. In the case of the test frames, they start at frame 20250 and end at frame 22450, which corresponds to the final portion of the video.

**The dataset is available for download** [**here**](https://zenodo.org/record/7944963#.ZGYoxHbMIQ8).

### Semantic Segmentation Models

#### U-NET Base & U-Net RED Architectures
These models is based on the architecture proposed by Ronneberger *et al* [[U-Net](https://arxiv.org/abs/1505.04597)].

<p align="center">
<img src="assets/unet_base.png" width="1000px"/>
</p>

#### U-NET 3D Architecture
This model is based on the architecture proposed by Çiçek *et al* [[3D U-Net](https://dl.acm.org/doi/abs/10.1007/978-3-319-46723-8_49)].
<p align="center">
<img src="assets/unet_3d.png" width="1000px"/>
</p>

### Results 

<div align="center">
<img src="assets/test_set_results.png" width="500px"/>
<p><strong>Performance metrics on the test set.</strong></p>
</div>

<div align="center">
<img src="assets/temporal_consitency.png" width="240px"/>
<p><strong>Average Temporal Consistency.</strong> The U-Net Base model, on average, has the
smallest TC value, which suggests that it has greater temporal consistency throughout the
video.</p>
</div>

<div align="center">
      <a href="https://www.youtube.com/watch?v=LvpJ7jXjSkw">
     <img 
      src="assets/play_video.png" 
      alt="U-Net Segmented Sequence and Original Dataset Video, side by side" 
      style="width:75%;">
      </a>
      <p><strong>U-Net Base</strong> Segmented Sequence and Original Dataset Video, side by side</p>
 </div>

### Paper Citation

To cite this work please use:
```bibtex
@article{ribeiro_ba_uav_article,
    title = {Burned area semantic segmentation: A novel dataset and evaluation using convolutional networks},
    journal = {ISPRS Journal of Photogrammetry and Remote Sensing},
    volume = {202},
    pages = {565-580},
    year = {2023},
    issn = {0924-2716},
    doi = {https://doi.org/10.1016/j.isprsjprs.2023.07.002},
    author = {Tiago F.R. Ribeiro and Fernando Silva and Jos\'e Moreira and Ro\'erio Lu\'is de C. Costa},
}
```

### Dataset Citation
```bibtex
@misc{ba_uav_ribeiro_dataset,
  author       = {Ribeiro, Tiago F. R. and Silva, Fernando and Moreira, Jos\'e and Costa, Ro\'erio Lu\'is de C.},
  title        = {BurnedAreaUAV Dataset (v1.1)},
  month        = may,
  year         = 2023,
  publisher    = {Zenodo},
  version      = {1.1},
  doi          = {10.5281/zenodo.7944963},
}
```

[//]: <> (### License )

### Acknowledgements

This work is partially funded by [FCT - Fundação para a Ciência e a Tecnologia, I.P.](https://www.fct.pt/), through projects MIT-EXPL/ACC/0057/2021 and UIDB/04524/2020, and under the Stimulus for Scientific Employment - Institutional Support - CEECINST/00051/2018.

### Contact

If you have any questions, suggestions or want to contribute, feel free to contact me at <code>tiago.r.ribeiro@gmail.com</code>.
