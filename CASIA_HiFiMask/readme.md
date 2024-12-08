=======================================================================
Paper: 
CASIA-SURF HiFiMask: Contrastive context-aware learning for 3d high-fidelity mask face presentation attack detection
========================================================================
Data decompression command: 
7za x CASIA-HiFi-Mask-crop3.zip -o./tmp/
After decompressing the data, place them in a folder named Data.
========================================================================

P1:
  Train:32,514(V)/325,139(I)
  Dev:4,347(V)/43,470(I)
  Test:17,362(V)/173,620(I)
P2.1
  Train:24,423(V)/244,229(I)
  Dev:3,264(V)/32,640(I)
  Test:8,661(V)/86,610(I)
P2.2
  Train:24,372(V)/243,720(I)
  Dev:3,258(V)/32,580(I)
  Test:8,685(V)/86,850(I)
P2.3
  Train:24,341(V)/243,409(I)
  Dev:3,256(V)/32,560(I)
  Test:8,686(V)/86,860(I)
P3
  Train:3,715(V)/37,150(I)
  Dev:536(V)/5,360(I)
  Test:17,362(V)/173,620(I)
  
========================================================================
Format:
Name: ComplexionID_SubjectID_TypeID_SceneID_LightID_SensorID.video
Complexion: Yellow(1), White(2), Black(3)
Subject: 01, 02, 03, ... , 75
Type: Live(0), Transparent(1), Plaster(2), Resin(3)
Scene: White(1), Green(2), Tricolor(3), Sunshine(4), Shadow(5), Motion(6)
Light: No(0), NormalLight(1), DimLight(2), BrightLight(3), BacklitLight(4),  SideSight(5), TopLight(6)
Sensor: SpO2(0), Iphone11(1), IphoneX(2), MI10(3), P40(4), S20(5), Vivo(6), D435(7), HJIM(8)
All Sensors:  75*4*(4*6*8 + 2*8) = 75*4*208 = 75*832 = 62400
Remove(D435): 75*4*(4*6*7 + 2*7) = 75*4*182 = 75*728 = 54600
========================================================================
Journals:
@article{liu2022contrastive,
  title={Contrastive context-aware learning for 3d high-fidelity mask face presentation attack detection},
  author={Liu, Ajian and Zhao, Chenxu and Yu, Zitong and Wan, Jun and Su, Anyang and Liu, Xing and Tan, Zichang and Escalera, Sergio and Xing, Junliang and Liang, Yanyan and others},
  journal={IEEE Transactions on Information Forensics and Security},
  volume={17},
  pages={2497--2507},
  year={2022},
  publisher={IEEE}
}
Conferences:
@inproceedings{liu20213d,
  title={3d high-fidelity mask face presentation attack detection challenge},
  author={Liu, Ajian and Zhao, Chenxu and Yu, Zitong and Su, Anyang and Liu, Xing and Kong, Zijian and Wan, Jun and Escalera, Sergio and Escalante, Hugo Jair and Lei, Zhen and others},
  booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision Workshops},
  pages={814--823},
  year={2021}
}
=======================================================================
Email: ajian.liu@ia.ac.cn, ajianliu92@gmail.com
Homepage: https://liuajian.github.io/
Github: https://github.com/liuajian
