=======================================================================
Paper: 
Unified Physical-Digital Face Attack Detection
After decompressing the data, place them in a folder named Data.
========================================================================

UniAttackData is an extension of CASIA-SURF CeFA, achieved through digital forgery. It encompasses
1,800 subjects from three ethnicities (such as African, East Asian, and Central Asian) and two 
types of physical attacks (Print and Replay). For each subject, we simulate 12 types of digital
attacks as follows:

(1) Pairing each subject with a image of others as the reference image.
(2) Utilizing the latest 6 digital editing algorithms and 6 adversarial algorithms on each live subject.
(3) To selectively manipulate only the facial region while retaining the background, our process initiates
face detection on every frames. Subsequently, we digitally alter solely the facial area and seamlessly 
integrate the background onto the modified face.

In summary, UniAttackData comprises live faces from three ethnicities, two types of print attacks in different
settings, one playback attack, as well as 6 digital editing attacks and 6 adversarial attacks.

========================================================================
(1) Protocol 1 aims to evaluate the unified attack detection task. Unlike traditional single-class attack detection, 
the unified attack data protocol encompasses both physical and digital attacks. The significant intra-class distance 
and diverse attacks pose more challenges to algorithm design. As shown in Table-1, the training, 
validation, and test sets include live faces and all attacks.

(2) Protocol 2 evaluates the generalization ability to "unseen" attack types. The vast differences and unpredictability 
between physical and digital attacks present challenges to algorithm portability. In this paper, we divide Protocol 2 
into two sub-protocols using the "leave-one-type-out testing" method, where the test sets for each sub-protocol consist 
of unseen attack types. As shown in Table-1, the test set of Protocol 2.1 contains only physical attacks 
unseen in the training and development sets, while the test set of Protocol 2.2 contains only digital attacks unseen in 
the training and development sets.

               Table-1:Amount of three different protocols
| Protocol | Class |# Live | # Phys | # Adv  | # Digital | # Total |
|----------|-------|-------|--------|--------|-------    |---------|
| P1       | train | 3000  | 1800   | 1800   | 1800      | 8400    |
|          | dev   | 1500  | 900    | 1800   | 1800      | 6000    |
|          | test  | 4500  | 2700   | 7106   | 7200      | 21506   |
| P2.1     | train | 3000  | 0      | 9000   | 9000      | 21000   |
|          | dev   | 1500  | 0      | 1706   | 1800      | 5006    |
|          | test  | 4500  | 5400   | 0      | 0         | 9900    |
| P2.2     | train | 3000  | 2700   | 0      | 0         | 5700    |
|          | dev   | 1500  | 2700   | 0      | 0         | 4200    |
|          | test  | 4500  | 0      | 10706  | 10800     | 26006   |

========================================================================

Correspondence between labels and attack types.
Protocol:
Live                ----> 1

Fake                ----> 0

Detailed_labels:
Live                ----> 0

Physical Attack     ----> 1

Adversarial Attack  ----> 2

Digital Attack      ----> 3
========================================================================

Conferences:
@inproceedings{fang2024unified,
  title     = {Unified Physical-Digital Face Attack Detection},
  author    = {Fang, Hao and Liu, Ajian and Yuan, Haocheng and Zheng, Junze and Zeng, Dingheng and Liu, Yanhong and Deng, Jiankang and Escalera, Sergio and Liu, Xiaoming and Wan, Jun and Lei, Zhen},
  journal={IJCAI},
  year={2024}
}
Conferences:
@article{yuan2024unified,
  title={Unified Physical-Digital Attack Detection Challenge},
  author={Yuan, Haocheng and Liu, Ajian and Zheng, Junze and Wan, Jun and Deng, Jiankang and Escalera, Sergio and Escalante, Hugo Jair and Guyon, Isabelle and Lei, Zhen},
  journal={CVPR Workshop},
  year={2024}
}
=======================================================================
Email: ajian.liu@ia.ac.cn, ajianliu92@gmail.com
Homepage: https://liuajian.github.io/
Github: https://github.com/liuajian
