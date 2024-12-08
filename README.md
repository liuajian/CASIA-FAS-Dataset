# How to install datasets

We suggest putting all datasets under the same folder (say `$DATA`=`CASIA_FAS_Dataset`) to ease management and following the instructions below to organize datasets to avoid modifying the source code. The file structure looks like

```
$DATA/
|–– CASIA_SURF/        
|–– CASIA_CeFA/       
|–– CASIA_HiFiMask/    
|–– CASIA_SuHiFiMask/  
|–– UniAttackData/     
```
If you have some datasets already installed somewhere else, you can create symbolic links in `$DATA/dataset_name` that point to the original data to avoid duplicate download.

Datasets list:
- [CASIA_SURF](#CASIA_SURF)              [[paper]](https://arxiv.org/pdf/1908.10654)
- [CASIA_CeFA](#CASIA_CeFA)              [paper](https://openaccess.thecvf.com/content/WACV2021/papers/Liu_CASIA-SURF_CeFA_A_Benchmark_for_Multi-Modal_Cross-Ethnicity_Face_Anti-Spoofing_WACV_2021_paper.pdf)
- [CASIA_HiFiMask](#CASIA_HiFiMask)      [paper](https://arxiv.org/pdf/2104.06148)
- [CASIA_SuHiFiMask](#CASIA_SuHiFiMask)  [paper](https://arxiv.org/pdf/2301.00975)
- [UniAttackData](#UniAttackData)        [paper](https://arxiv.org/pdf/2401.17699)

The instructions to prepare each dataset are detailed below. To ensure reproducibility and fair comparison for future work, we provide fixed train/dev/test protocols for all datasets. The fixed protocols are either from the original datasets (if available) or created by us.

### CASIA_SURF
- Create a folder named `CASIA_SURF/` under `$DATA`.
- Create `Data/` under `CASIA_SURF/`.
- Create `protocol/` under `CASIA_SURF/`.
- Or download the dataset from the [official website](https://sites.google.com/view/face-anti-spoofing-challenge/dataset-download/casia-surfcvpr2019?authuser=0) and extract the Training, Val and Testing sets to `$DATA/CASIA_SURF/Data`.
- Decompression instruction: 7za x CASIA_SURF.7z

The directory structure should look like
```
CASIA_SURF/
|–– Data/
|   |–– Training/
|   |   |–– real_part/  # contains 300 folders like CLKJ_AS0005, CLKJ_AS0011, etc.
|   |   |–– fake_part/  # contains 300 folders
|   |–– Val/
|   |   |–– real_part/  # contains 100 folders
|   |   |–– fake_part/  # contains 100 folders
|   |–– Testing/
|   |   |–– real_part/  # contains 600 folders
|   |   |–– fake_part/  # contains 600 folders
|–– protocol/
|   |–– CASIA_SURF@p1_image_train.txt  # contains all image paths and their labels.
|   |–– CASIA_SURF@p1_image_dev.txt
|   |–– CASIA_SURF@p1_image_test.txt
|   |–– CASIA_SURF@p1_video_train.txt  # contains all video paths and their labels.
|   |–– CASIA_SURF@p1_video_dev.txt
|   |–– CASIA_SURF@p1_video_test.txt
```
- If you had downloaded the CASIA_SURF dataset before, you can create symbolic links to map the Training, Val and Testing sets to `$DATA/CASIA_SURF/Data`.
- You need to download the protocol again and place it in the `$DATA/CASIA_SURF/protocol`.

### CASIA_CeFA
- Create a folder named `CASIA_CeFA/` under `$DATA`.
- Create `protocol/` under `CASIA_CeFA/`.
- Or download the dataset from the [official website](https://sites.google.com/view/face-anti-spoofing-challenge/dataset-download/casia-surf-cefacvpr2020?authuser=0) and extract the Ethnicity and Mask sets to `$DATA/CASIA_CeFA`.
- Decompression instruction: 7za x CASIA_CeFA.7z

The directory structure should look like
```
CASIA_CeFA/
|–– Ethnicity/
|   |–– AF/             # contains 500 folders like AF-000, AF-001, etc.
|   |–– CA/
|   |–– EA/
|–– Mask/
|   |–– 3D-Mask/        # contains 99 folders
|   |–– Silicone-Mask/  # contains 8 folders
|–– protocol/
|   |–– CASIA_CeFA@p1.1_image_train.txt
|   |–– CASIA_CeFA@p1.1_image_dev.txt
|   |–– CASIA_CeFA@p1.1_image_test.txt
|   |–– CASIA_CeFA@p1.3_image_train.txt
|   |–– CASIA_CeFA@p1.3_image_dev.txt
|   |–– CASIA_CeFA@p1.3_image_test.txt
|   |–– CASIA_CeFA@p1.5_image_train.txt
|   |–– CASIA_CeFA@p1.5_image_dev.txt
|   |–– CASIA_CeFA@p1.5_image_test.txt
|   |–– CASIA_CeFA@p2.1_image_train.txt
|   |–– CASIA_CeFA@p2.1_image_dev.txt
|   |–– CASIA_CeFA@p2.1_image_test.txt
|   |–– CASIA_CeFA@p2.2_image_train.txt
|   |–– CASIA_CeFA@p2.2_image_dev.txt
|   |–– CASIA_CeFA@p2.2_image_test.txt
|   |–– CASIA_CeFA@p3_image_train.txt
|   |–– CASIA_CeFA@p3_image_dev.txt
|   |–– CASIA_CeFA@p3_image_test.txt
|   |–– CASIA_CeFA@p4.1_image_train.txt
|   |–– CASIA_CeFA@p4.1_image_dev.txt
|   |–– CASIA_CeFA@p4.1_image_test.txt
|   |–– CASIA_CeFA@p4.3_image_train.txt
|   |–– CASIA_CeFA@p4.3_image_dev.txt
|   |–– CASIA_CeFA@p4.3_image_test.txt
|   |–– CASIA_CeFA@p4.5_image_train.txt
|   |–– CASIA_CeFA@p4.5_image_dev.txt
|   |–– CASIA_CeFA@p4.5_image_test.txt
```

### CASIA_HiFiMask
- Create a folder named `CASIA_HiFiMask/` under `$DATA`.
- Create `Data/` under `CASIA_HiFiMask/`.
- Create `protocol/` under `CASIA_HiFiMask/`.
- Or download the dataset from the [official website](https://sites.google.com/view/face-anti-spoofing-challenge/dataset-download/casia-surf-hifimaskiccv2021?authuser=0) and extract the video folders to `$DATA/CASIA_HiFiMask/Data`.
- Decompression instruction: 7za x CASIA-HiFi-Mask-crop3.zip -o./Data/

The directory structure should look like
```
CASIA_HiFiMask/
|–– Data/          # contains 54,223 folders like 1_01_0_1_1_1, 1_01_0_1_1_2, etc.
|–– protocol/
|   |–– CASIA_HiFiMask@p1_image_train.txt
|   |–– CASIA_HiFiMask@p1_image_dev.txt
|   |–– CASIA_HiFiMask@p1_image_test.txt
|   |–– CASIA_HiFiMask@p2.1_image_train.txt
|   |–– CASIA_HiFiMask@p2.1_image_dev.txt
|   |–– CASIA_HiFiMask@p2.1_image_test.txt
|   |–– CASIA_HiFiMask@p2.2_image_train.txt
|   |–– CASIA_HiFiMask@p2.2_image_dev.txt
|   |–– CASIA_HiFiMask@p2.2_image_test.txt
|   |–– CASIA_HiFiMask@p2.3_image_train.txt
|   |–– CASIA_HiFiMask@p2.3_image_dev.txt
|   |–– CASIA_HiFiMask@p2.3_image_test.txt
|   |–– CASIA_HiFiMask@p3_image_train.txt
|   |–– CASIA_HiFiMask@p3_image_dev.txt
|   |–– CASIA_HiFiMask@p3_image_test.txt
```

### CASIA_SuHiFiMask
- Create a folder named `CASIA_SuHiFiMask/` under `$DATA`.
- Create `Data/` under `CASIA_SuHiFiMask/`.
- Create `protocol/` under `CASIA_SuHiFiMask/`.
- Or download the dataset from the [official website](https://sites.google.com/view/face-anti-spoofing-challenge/dataset-download/casia-surf-suhifimaskcvpr2023?authuser=0) and extract the video folders to `$DATA/CASIA_SuHiFiMask/Data`.
- Decompression instruction: 7za x SuHiFiMask_TIFS24.7z

The directory structure should look like
```
CASIA_HiFiMask/
|–– Data/   # contains 10,128 folders like G01_S1_C1_E01_T20220117102532743, G01_S1_C1_E02_T20220117103654331, etc.
|–– protocol/
|   |–– CASIA_SuHiFiMask@p1_image_train.txt
|   |–– CASIA_SuHiFiMask@p1_image_dev.txt
|   |–– CASIA_SuHiFiMask@p1_image_test.txt
|   |–– CASIA_SuHiFiMask@p2.1_image_train.txt
|   |–– CASIA_SuHiFiMask@p2.1_image_dev.txt
|   |–– CASIA_SuHiFiMask@p2.1_image_test.txt
|   |–– CASIA_SuHiFiMask@p2.2_image_train.txt
|   |–– CASIA_SuHiFiMask@p2.2_image_dev.txt
|   |–– CASIA_SuHiFiMask@p2.2_image_test.txt
|   |–– CASIA_SuHiFiMask@p2.3_image_train.txt
|   |–– CASIA_SuHiFiMask@p2.3_image_dev.txt
|   |–– CASIA_SuHiFiMask@p2.3_image_test.txt
|   |–– CASIA_SuHiFiMask@p2.4_image_train.txt
|   |–– CASIA_SuHiFiMask@p2.4_image_dev.txt
|   |–– CASIA_SuHiFiMask@p2.4_image_test.txt
|   |–– CASIA_SuHiFiMask@p3_image_train.txt
|   |–– CASIA_SuHiFiMask@p3_image_dev.txt
|   |–– CASIA_SuHiFiMask@p3_image_test.txt
```

### UniAttackData
- Create a folder named `UniAttackData/` under `$DATA`.
- Create `Data/` under `UniAttackData/`.
- Create `protocol/` under `UniAttackData/`.
- Or download the dataset from the [official website](https://sites.google.com/view/face-anti-spoofing-challenge/dataset-download/uniattackdatacvpr2024?authuser=0) and extract the video folders to `$DATA/UniAttackData/Data`.

The directory structure should look like
```
CASIA_HiFiMask/
|–– Data/          
|   |–– adv-attacks
|   |–– DaGAN
|   |–– FaceDancer
|   |–– InsightFace
|   |–– live
|   |–– OneShotTH
|   |–– SAFA
|   |–– simswap
|   |–– spoof
|–– protocol/
|   |–– UniAttackData@p1_image_train.txt
|   |–– UniAttackData@p1_image_dev.txt
|   |–– UniAttackData@p1_image_test.txt
|   |–– UniAttackData@p2.1_image_train.txt
|   |–– UniAttackData@p2.1_image_dev.txt
|   |–– UniAttackData@p2.1_image_test.txt
|   |–– UniAttackData@p2.2_image_train.txt
|   |–– UniAttackData@p2.2_image_dev.txt
|   |–– UniAttackData@p2.2_image_test.txt
```

### Citation
  ```Shell
Please cite the following papers in your publications if it helps your research:
 
## CASIA-SURF
@article{zhang2020casia,
  title={Casia-surf: A large-scale multi-modal benchmark for face anti-spoofing},
  author={Zhang, Shifeng and Liu, Ajian and Wan, Jun and Liang, Yanyan and Guo, Guodong and Escalera, Sergio and Escalante, Hugo Jair and Li, Stan Z},
  journal={IEEE Transactions on Biometrics, Behavior, and Identity Science},
  volume={2},
  number={2},
  pages={182--193},
  year={2020},
  publisher={IEEE}
}

@inproceedings{liu2019multi,
  title={Multi-modal face anti-spoofing attack detection challenge at cvpr2019},
  author={Liu, Ajian and Wan, Jun and Escalera, Sergio and Jair Escalante, Hugo and Tan, Zichang and Yuan, Qi and Wang, Kai and Lin, Chi and Guo, Guodong and Guyon, Isabelle and others},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops},
  pages={0--10},
  year={2019}
}

## CASIA-CeFA
@inproceedings{liu2021casia,
  title={Casia-surf cefa: A benchmark for multi-modal cross-ethnicity face anti-spoofing},
  author={Liu, Ajian and Tan, Zichang and Wan, Jun and Escalera, Sergio and Guo, Guodong and Li, Stan Z},
  booktitle={Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision},
  pages={1179--1187},
  year={2021}
}

@article{liu2021cross,
  title={Cross-ethnicity face anti-spoofing recognition challenge: A review},
  author={Liu, Ajian and Li, Xuan and Wan, Jun and Liang, Yanyan and Escalera, Sergio and Escalante, Hugo Jair and Madadi, Meysam and Jin, Yi and Wu, Zhuoyuan and Yu, Xiaogang and others},
  journal={IET Biometrics},
  volume={10},
  number={1},
  pages={24--43},
  year={2021},
  publisher={Wiley Online Library}
}

## CASIA-HiFiMask
@article{liu2022contrastive,
  title={Contrastive context-aware learning for 3d high-fidelity mask face presentation attack detection},
  author={Liu, Ajian and Zhao, Chenxu and Yu, Zitong and Wan, Jun and Su, Anyang and Liu, Xing and Tan, Zichang and Escalera, Sergio and Xing, Junliang and Liang, Yanyan and others},
  journal={IEEE Transactions on Information Forensics and Security},
  volume={17},
  pages={2497--2507},
  year={2022},
  publisher={IEEE}
}

@inproceedings{liu20213d,
  title={3d high-fidelity mask face presentation attack detection challenge},
  author={Liu, Ajian and Zhao, Chenxu and Yu, Zitong and Su, Anyang and Liu, Xing and Kong, Zijian and Wan, Jun and Escalera, Sergio and Escalante, Hugo Jair and Lei, Zhen and others},
  booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision Workshops},
  pages={814--823},
  year={2021}
}

## UniAttackData
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



