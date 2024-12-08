### Paper: CASIA-SuHiFiMask: Surveillance Face Anti-spoofing

### Data decompression command: 7za x SuHiFiMask_TIFS24.7z After decompressing the data, place them in a folder named Data.

### Protocol:
```
P1
  Train:72,217(V)/201,568(I)
  Dev:12,082(V)/40,824(I)
  Test:64,441(V)/132,190(I)
P2.1
  Train:83,528(V)/141,444(I)
  Dev:32,184(V)/40,129(I)
  Test:22,155(V)/63,738(I)
P2.2
  Train:68,783(V)/115,790(I)
  Dev:31,604(V)/39,557(I)
  Test:23,886(V)/70,887(I)
P2.3
  Train:64,571(V)/106,946(I)
  Dev:30,639(V)/38,308(I)
  Test:28,131(V)/86,602(I)
P2.4
  Train:65,326(V)/108,189(I)
  Dev:30,939(V)/38,695(I)
  Test:27,683(V)/85,400(I)
P3
  Train:39,370(V)/159,063(I)
  Dev:41,997(V)/89,276(I)
  Test:58,652(V)/164,557(I)
```

### Format:
```
For the meaning of each line in the protocol txt file (taking an entry as an example), such as G05_S30_C3_E03_T20220227113320490/id_4/120_43_0.jpg,0.

In the identifier G05_S30_C3_E03_T20220227113320490, the abbreviations G, S, C, E, and T actually stand for GroupID, SceneID, CameraID, EpochID, and Time, respectively. 
(1) SceneID ranges from 01 to 40 for different surveillance scenes. 
(2) CameraID represents the capture device. 
(3) EpochID and GroupID represent a particular round of shooting for a particular group of subjects. 
(4) Time records the time the video was taken. Please note that the subdirectory id_4 only represents the participant's ID for this round of shooting and is not the participant ID specified in the paper.

For each image with a name such as 120_43_0.jpg, where 120 is the frame number in the video, 43 represents the participant's ID, and 0 is the category label. This is analogous to the meaning conveyed by the final number in this line, both indicating the label of the respective image.
```

### Acknowledgements
```
@article{fang2023surveillance,
  title={Surveillance Face Anti-spoofing},
  author={Fang, Hao and Liu, Ajian and Wan, Jun and Escalera, Sergio and Zhao, Chenxu and Zhang, Xu and Li, Stan Z and Lei, Zhen},
  journal={IEEE Transactions on Information Forensics and Security},
  year={2023}
}

@inproceedings{escalera2023surveillance,
  title={Surveillance Face Presentation Attack Detection Challenge},
  author={Fang, Hao, Liu, Ajian and Wan, Jun, Escalera, Sergio and Escalante, Hugo Jair and Lei, Zhen},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshop},
  pages={6360--6370},
  year={2023}
}
```

### Contact
Email: ajian.liu@ia.ac.cn
Homepage: https://liuajian.github.io/

