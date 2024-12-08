### Paper: CASIA-SURF CeFA: A Benchmark for Multi-modal Cross-ethnicity Face Anti-spoofing

### Label: live:0/fake:1

### Protocol:
```
p1.1:(AF&AF-CA/EA)
  Train:800(V)/71,915(I)
  Dev:400(V)/36,298(I)
  Test:2,723(V)/191,161(I)
p1.3:(CA&CA-AF/EA)
  Train:800(V)/73,304(I)
  Dev:400(V)/37,855(I)
  Test:2,723(V)/185,833(I)
p1.5:(EA&EA-AF/CA)
  Train:800(V)/71,704(I)
  Dev:400(V)/36,193(I)
  Test:2,723(V)/188,100(I)
  
p2.1:(Cloth&Cloth-Screen)
  Train:1,800(V)/166,255(I)
  Dev:900(V)/83,499(I)
  Test:2,323(V)/151,807(I)
p2.2:(Screen&Screen-Cloth)
  Train:1,200(V)/109,632(I)
  Dev:600(V)/56,070(I)
  Test:2,923(V)/210,252(I)

p3:(color)
  Train:216,923(I)
  Dev:110,346(I)
  Test:438,764(I)

p4.1:(AF&AF@Screen-CA/EA@Cloth)
  Train:400(V)/36,513(I)
  Dev:200(V)/18,468(I)
  Test:2,323(V)/155,967(I)
p4.3:(CA&CA@Screen-AF/EA@Cloth)
  Train:400(V)/37,167(I)
  Dev:200(V)/19,093(I)
  Test:2,323(V)/152,717(I)
p4.5:(EA&EA@Screen-AF/CA@Cloth)
  Train:400(V)/35,952(I)
  Dev:200(V)/18,509(I)
  Test:2,323(V)/153,930(I)
```

### Modality:, color, depth, ir

### Formta:
```
Datasets: Specifically for 3 ethnic datasets
Format: Race/Race-ID-IdCard/Race_ID_AcqDevice_Session_PAI
    Race: 1:AF 2:CA 3:EA
    ID: 000-499
    IdCard: 
        (1) The first four digits represent the year of birth; 
        (2) The penultimate digit represents gender, with even numbered females (F) penultimate and odd numbered males (M).
    AcqDevice: 1:rssdk 2:mp4  3:bag 4:MOV
    Session(environment): 1:indoor 2:outdoor 3:random
    PAI: 1:Real 2:Cloth 3:Pic(phtoto) 4:Screen
Example: EA/EA-012-198006250024/1_000_1_1_1(P1_P2_P3_P4_P5). Age:1980, Gender: F.

Datasets: 3D-Mask
Format: 3D-Mask/ID/3DMASK_ID_If-Dresses_If-Glasses_AcqDevice_Session_AttackType
    3DMASK: 1
    ID:002-100
    If-Dresses: 0:No_Dresses 1:Dresses
    If-Glasses: 0:No_Glasses 1:Glasses
    AcqDevice: 1:Camera 2:D435i
    Session(environment): 1:Indoor 2:Outdoor
    AttackType(environment): 1:NoLighting 2:BackLighting 3:AlongLighting 4:SideLighting
Example:3D-MASK/ID/3DMASK_ID_Dresses_Glasses_D435i_Indoor_AlongLighting(P0,P1,P2,P3,P4,P5,P6)
Format: 3D-MASK/002/1_002_1_1_2_1_3

Datasets: Silicione-Mask
Format: Silicone-Mask/ID/SiliconeMask_ID_Dresses_If-Glasses_AcqDevice_Session_AttackType
    SiliconeMask: 2
    ID: 001-008
    Dresses: 1:Dresses
    If-Glasses: 0:No_Glasses 1:Glasses
    AcqDevice: 1:Camera 2:D435i
    Session(environment): 1:Indoor
    AttackType(environment): 1:NoLighting 2:BackLighting 3:AlongLighting 4:SideLighting
Example: mean:Silicone-Mask/ID/SiliconeMask_ID_Dresses_Glasses_D435i_Indoor_AlongLighting(P0,P1,P2,P3,P4,P5,P6)
Format:       Silicone-Mask/001/2_001_1_1_2_1_3
```

### Acknowledgements
```
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
```

### Contact
Email: ajian.liu@ia.ac.cn
Homepage: https://liuajian.github.io/

