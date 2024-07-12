<div align="center">
<h1> Awesome-Scene-Graph-for-Cross-Modal-Learning </h1> 
</div>




# 🎨 Introduction 
A scene graph is a topological structure representing a scene described in text, image, video, or etc. 
In this graph, the nodes correspond to object bounding boxes with their category labels and attributes, while the edges represent the pair-wise relationships between objects. 
  <p align="center">
  <img src="assets/intro1.png" width="75%">
</p>

---

# 📕 Table of Contents
- [🎨 Introduction](#-introduction)
- [📕 Table of Contents](#-contents)
- [🌷 Scene Graph Datasets](#-datasets)
- [🍕 Scene Graph Generation](#-scene-graph-generation)
  - [2D (Image) Scene Graph Generation](#2d-image-scene-graph-generation)
  - [Spatio-Temporal (Video) Scene Graph Generation](#spatio-temporal-video-scene-graph-generation)
  - [Audio Scene Graph Generation](#audio-scene-graph-generation)
  - [3D Scene Graph Generation](#3d-scene-graph-generation)
  - [Textual Scene Graph Generation](#textual-scene-graph-generation)
- [🥝 Scene Graph Application](#-scene-graph-application)
  - [Image Retrieval](#image-retrieval)
  - [2D Image Generation](#2d-image-generation)
  - [3D Generation](#3d-generation)
  - [Visual Question Answering](#visual-question-answering)
  - [Mitigate Hallucination](#mitigate-hallucination)
  - [Dynamic Environment Guidance](#dynamic-environment-guidance)
  - [Privacy-sensitive Object Identification](#privacy-sensitive-object-identification)
  - [Image Captioning](#)
  - [Video Retrieval](#video-retrieval)
- [🤶 Evaluation Metrics](#evaluation-metrics)
- [🐱‍🚀 Miscellaneous](#miscellaneous)
  - [Toolkit](#toolkit)
  - [Workshop](#workshop)
  - [Survey](#survey)
- [⭐️ Star History](#️-star-history)


---


# 🌷 Scene Graph Datasets
<p align="center">

| Dataset |  Modality  |   Obj. Class  | BBox | Rela. Class | Triplets | Instances | 
|:--------:|:--------:|:--------:| :--------:|  :--------:|  :--------:|  :--------:|
| [Visual Phrase](https://vision.cs.uiuc.edu/phrasal/) | Image | 8 | 3,271 | 9 | 1,796 | 2,769 |
| [Scene Graph](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) | Image | 266 | 69,009 | 68 | 109,535 | 5,000 |
| [VRD](https://cs.stanford.edu/people/ranjaykrishna/vrd/)  | Image | 100 | - | 70 | 37,993 | 5,000 |
| [Open Images v7](https://storage.googleapis.com/openimages/web/index.html)  | Image | 57 | 3,290,070 | 329 | 374,768 | 9,178,275 |
| [Visual Genome](https://homes.cs.washington.edu/~ranjay/visualgenome/index.html) | Image | 33,877 | 3,843,636 | 40,480 | 2,347,187 | 108,077 | 
| [VrR-VG](http://vrrvg.com/) | Image | 1,600 | 282,460 | 117 | 203,375 | 58,983 |
| [UnRel](https://www.di.ens.fr/willow/research/unrel/) | Image | - | - | 18 | 76 |  1,071 |
| [SpatialSense](https://github.com/princeton-vl/SpatialSense) | Image | 3,679 | - | 9 | 13,229 | 11,569 |
| [SpatialVOC2K](https://github.com/muskata/SpatialVOC2K) | Image | 20 | 5,775 | 34 | 9,804 | 2,026 | 
| [OpenSG](https://github.com/Jingkang50/OpenPSG) | Image (panoptic) | 133 | - | 56 | - | 49K |
| [AUG](https://arxiv.org/pdf/2404.07788) | Image (Overhead View) | 76 | - | 61 | - | - |
| [STAR](https://arxiv.org/pdf/2406.09410) | Satellite Imagery | 48 | 219,120 | 58 | 400,795 | 31,096 |
| [ReCon1M](https://arxiv.org/pdf/2406.06028) | Satellite Imagery | 60 |  859,751 | 64 | 1,149,342 |  21,392 |
| [SkySenseGPT](https://github.com/Luo-Z13/SkySenseGPT) | Satellite Imagery (Instruction) | - | - | - | - | - |
| [ImageNet-VidVRD](https://xdshang.github.io/docs/imagenet-vidvrd.html) | Video | 35 | - | 132 | 3,219 | 100 |
| [VidOR](https://xdshang.github.io/docs/vidor.html) | Video | 80 | - | 50 | - | 10,000 |
| [Action Genome](https://github.com/JingweiJ/ActionGenome) | Video | 35 | 0.4M | 25 | 1.7M | 10,000 |
| [AeroEye](https://arxiv.org/pdf/2406.01029) | Video (Drone-View) | 56 | - | 384 | - | 2.2M |
| [PVSG](https://jingkang50.github.io/PVSG/) | Video (panoptic) | 126 | - |  57 |  - | 400|
| [ASPIRe](https://uark-cviu.github.io/ASPIRe/) | Video(Interlacements) | - | - | 4.5K | - | 1.5K |
| [3D Semantic Scene Graphs (3DSSG)](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wald_Learning_3D_Semantic_Scene_Graphs_From_3D_Indoor_Reconstructions_CVPR_2020_paper.pdf) | 3D | 40 | - | - | - | 48K|
| [PSG4D](https://arxiv.org/pdf/2405.10305) | 4D | 46 | - | 15 | - | - | - |
| [FACTUAL](https://github.com/zhuang-li/FactualSceneGraph) | Text | - | - | - | - | 40,369 |
</p>


---

<!-- CVPR-8A2BE2 -->
<!-- WACV-6a5acd -->
<!-- NIPS-CD5C5C -->
<!-- ICML-FF7F50 -->
<!-- ICCV-00CED1 -->
<!-- ECCV-1e90ff -->
<!-- TPAMI-BC8F8F -->
<!-- IJCAI-228b22 -->
<!-- AAAI-c71585 -->
<!-- arXiv-b22222 -->
<!-- ACL-191970 -->
<!-- TPAMI-ffa07a -->


# 🍕 Scene Graph Generation

## 2D (Image) Scene Graph Generation

There are three subtasks:
- `Predicate classification`: given ground-truth labels and bounding boxes of object pairs, predict the predicate label.
- `Scene graph classification`: joint classification of predicate labels and the objects' category given the grounding bounding boxes.
- `Scene graph detection`: detect the objects and their categories, and predict the predicate between object pairs.

### LLM-based 

+ [**Scene Graph Generation Strategy with Co-occurrence Knowledge and Learnable Term Frequency**](https://arxiv.org/pdf/2405.12648) [![Paper](https://img.shields.io/badge/ICML24-FF7F50)]() 

+ [**SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding**](https://arxiv.org/pdf/2406.10100) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Luo-Z13/SkySenseGPT.svg?style=social&label=Star)](https://github.com/Luo-Z13/SkySenseGPT) 

+ [**VLPrompt: Vision-Language Prompting for Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2311.16492) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/franciszzj/VLPrompt.svg?style=social&label=Star)](https://github.com/franciszzj/VLPrompt) 

+ [**From Pixels to Graphs: Open-Vocabulary Scene Graph Generation with Vision-Language Models**](https://arxiv.org/pdf/2404.00906) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/SHTUPLUS/Pix2Grp_CVPR2024.svg?style=social&label=Star)](https://github.com/SHTUPLUS/Pix2Grp_CVPR2024) 

+ [**LLM4SGG: Large Language Models for Weakly Supervised Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2024/papers/Kim_LLM4SGG_Large_Language_Models_for_Weakly_Supervised_Scene_Graph_Generation_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/rlqja1107/torch-LLM4SGG.svg?style=social&label=Star)](https://github.com/rlqja1107/torch-LLM4SGG) 

+ [**Visually-Prompted Language Model for Fine-Grained Scene Graph Generation in an Open World**](https://openaccess.thecvf.com/content/ICCV2023/papers/Yu_Visually-Prompted_Language_Model_for_Fine-Grained_Scene_Graph_Generation_in_an_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]()  [![Star](https://img.shields.io/github/stars/Yuqifan1117/CaCao.svg?style=social&label=Star)](https://github.com/Yuqifan1117/CaCao) 


+ [**GPT4SGG: Synthesizing Scene Graphs from Holistic and Region-specific Narratives**](https://arxiv.org/pdf/2312.04314) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://gpt4vision.github.io/gpt4sgg/)

+ [**Expanding Scene Graph Boundaries: Fully Open-vocabulary Scene Graph Generation via Visual-Concept Alignment and Retention**](https://arxiv.org/pdf/2311.10988) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]()

+ [**Less is More: Toward Zero-Shot Local Scene Graph Generation via Foundation Models**](https://arxiv.org/pdf/2310.01356)  [![Paper](https://img.shields.io/badge/arXiv23-b22222)]()


+ [**Enhancing Scene Graph Generation with Hierarchical Relationships and Commonsense Knowledge**](https://arxiv.org/pdf/2311.12889) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() [![Star](https://img.shields.io/github/stars/bowen-upenn/scene_graph_commonsense.svg?style=social&label=Star)](https://github.com/bowen-upenn/scene_graph_commonsense) 🙆‍♀️👈 


### Non-LLM-based

+ [**Leveraging Predicate and Triplet Learning for Scene Graph Generation**](https://arxiv.org/pdf/2406.02038) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/jkli1998/DRM.svg?style=social&label=Star)](https://github.com/jkli1998/DRM) 
 

+ [**DSGG: Dense Relation Transformer for an End-to-end Scene Graph Generation**](https://arxiv.org/pdf/2403.14886) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/zeeshanhayder/DSGG.svg?style=social&label=Star)](https://github.com/zeeshanhayder/DSGGM) 

+ [**HiKER-SGG: Hierarchical Knowledge Enhanced Robust Scene Graph Generation**](https://arxiv.org/pdf/2403.12033) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/zhangce01/HiKER-SGG.svg?style=social&label=Star)](https://github.com/zhangce01/HiKER-SGG)


+ [**EGTR: Extracting Graph from Transformer for Scene Graph Generation**](https://arxiv.org/pdf/2404.02072) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/naver-ai/egtr.svg?style=social&label=Star)](https://github.com/naver-ai/egtr) 

+ [**STAR: A First-Ever Dataset and A Large-Scale Benchmark for Scene Graph Generation in Large-Size Satellite Imagery**](https://arxiv.org/pdf/2406.09410) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Zhuzi24/SGG-ToolKit.svg?style=social&label=Star)](https://github.com/Zhuzi24/SGG-ToolKit) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://linlin-dev.github.io/project/STAR)

+ [**Improving Scene Graph Generation with Relation Words’ Debiasing in Vision-Language Models**](https://arxiv.org/pdf/2403.16184) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**Adaptive Visual Scene Understanding: Incremental Scene Graph Generation**](https://arxiv.org/pdf/2310.01636)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**ReCon1M:A Large-scale Benchmark Dataset for Relation Comprehension in Remote Sensing Imagery**](https://arxiv.org/pdf/2406.06028) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Reltr: Relation transformer for scene graph generation**](https://arxiv.org/abs/2201.11460) [![Paper](https://img.shields.io/badge/TPAMI23-ffa07a)]()  [![Star](https://img.shields.io/github/stars/yrcong/RelTR.svg?style=social&label=Star)](https://github.com/yrcong/RelTR)

+ [**Unbiased Scene Graph Generation via Two-stage Causal Modeling**](https://arxiv.org/pdf/2307.05276) [![Paper](https://img.shields.io/badge/TPAMI23-ffa07a)]()

+ [**Zero-Shot Scene Graph Generation via Triplet Calibration and Reduction**](https://arxiv.org/pdf/2309.03542) [![Paper](https://img.shields.io/badge/TOMM23-ffa07a)]() [![Star](https://img.shields.io/github/stars/jkli1998/T-CAR.svg?style=social&label=Star)](https://github.com/jkli1998/T-CAR) 

+ [**Evidential Unvertainty and Diversity Guided Active Learning for Scene Graph Generation**](https://openreview.net/pdf?id=xI1ZTtVOtlz) [![Paper](https://img.shields.io/badge/ICLR23-696969)]()

+ [**Prototype-based Embedding Network for Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Zheng_Prototype-Based_Embedding_Network_for_Scene_Graph_Generation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/VL-Group/PENET.svg?style=social&label=Star)]([VL-Group/PENET](https://github.com/VL-Group/PENET))

+ [**IS-GGT: Iterative Scene Graph Generation With Generative Transformers**](https://openaccess.thecvf.com/content/CVPR2023/papers/Kundu_IS-GGT_Iterative_Scene_Graph_Generation_With_Generative_Transformers_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]()

+ [**SGTR: End-to-end Scene Graph Generation with Transformer**](https://arxiv.org/pdf/2112.12970) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Star](https://img.shields.io/github/stars/Scarecrow0/SGTR.svg?style=social&label=Star)](https://github.com/Scarecrow0/SGTR)


+ [**Unsupervised Vision-Language Parsing: Seamlessly Bridging Visual Scene Graphs with Language Structures via Dependency Relationships**](https://openaccess.thecvf.com/content/CVPR2022/papers/Lou_Unsupervised_Vision-Language_Parsing_Seamlessly_Bridging_Visual_Scene_Graphs_With_Language_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Star](https://img.shields.io/github/stars/LouChao98/VLGAE.svg?style=social&label=Star)](https://github.com/LouChao98/VLGAE)


+ [**Fine-Grained Scene Graph Generation with Data Transfer**](https://arxiv.org/pdf/2203.11654) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]() [![Star](https://img.shields.io/github/stars/waxnkw/IETrans-SGG.pytorch.svg?style=social&label=Star)](https://github.com/waxnkw/IETrans-SGG.pytorch)

+ [**Iterative Scene Graph Generation**](https://proceedings.neurips.cc/paper_files/paper/2022/file/99831104028c3b7e6079fd8bdcc42c8f-Paper-Conference.pdf) [![Paper](https://img.shields.io/badge/NIPS22-CD5C5C2)]() [![Star](https://img.shields.io/github/stars/ubc-vision/IterativeSG.svg?style=social&label=Star)](https://github.com/ubc-vision/IterativeSG)

+ [**GPS-Net: Graph Property Sensing Network for Scene Graph Generation**](https://arxiv.org/pdf/2003.12962) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/siml3/GPS-Net.svg?style=social&label=Star)](https://github.com/siml3/GPS-Net)


+ [**Graphical Contrastive Losses for Scene Graph Parsing**](https://openaccess.thecvf.com/content_CVPR_2019/papers/Zhang_Graphical_Contrastive_Losses_for_Scene_Graph_Parsing_CVPR_2019_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR19-8A2BE2)]() [![Star](https://img.shields.io/github/stars/NVIDIA/ContrastiveLosses4VRD.svg?style=social&label=Star)](https://github.com/NVIDIA/ContrastiveLosses4VRD)

+ [**Learning to Compose Dynamic Tree Structures for Visual Contexts**](https://openaccess.thecvf.com/content_CVPR_2019/papers/Tang_Learning_to_Compose_Dynamic_Tree_Structures_for_Visual_Contexts_CVPR_2019_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR19-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/KaihuaTang/VCTree-Scene-Graph-Generation.svg?style=social&label=Star)](https://github.com/KaihuaTang/VCTree-Scene-Graph-Generation)

+ [**Neural motifs: Scene graph parsing with global context**](https://openaccess.thecvf.com/content_cvpr_2018/papers/Zellers_Neural_Motifs_Scene_CVPR_2018_paper.pdf)  [![Paper](https://img.shields.io/badge/CVPR18-8A2BE2)]() [![Star](https://img.shields.io/github/stars/rowanz/neural-motifs.svg?style=social&label=Star)](https://github.com/rowanz/neural-motifs)

+ [**Scene Graph Generation From Objects, Phrases and Region Captions**](https://openaccess.thecvf.com/content_ICCV_2017/papers/Li_Scene_Graph_Generation_ICCV_2017_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV17-2f4f4f)]() [![Star](https://img.shields.io/github/stars/yikang-li/MSDN.svg?style=social&label=Star)](https://github.com/yikang-li/MSDN)

+ [**Visual Relationship Detection with Language Priors**](https://arxiv.org/pdf/1608.00187) [![Paper](https://img.shields.io/badge/ECCV16-1e90ff)]() [![Star](https://img.shields.io/github/stars/Prof-Lu-Cewu/Visual-Relationship-Detection.svg?style=social&label=Star)](https://github.com/Prof-Lu-Cewu/Visual-Relationship-Detection)



## Panoptic Scene Graph Generation

+ [**Panoptic scene graph generation with semantics-prototype learning**](https://ojs.aaai.org/index.php/AAAI/article/view/28098)[![Paper](https://img.shields.io/badge/AAAI24-c71585)]() [![Star](https://img.shields.io/github/stars/lili0415/PSG-biased-annotation.svg?style=social&label=Star)](https://github.com/lili0415/PSG-biased-annotation)

+ [**TextPSG: Panoptic Scene Graph Generation from Textual Descriptions**](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhao_TextPSG_Panoptic_Scene_Graph_Generation_from_Textual_Descriptions_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]() [![Star](https://img.shields.io/github/stars/chengyzhao/TextPSG.svg?style=social&label=Star)](https://github.com/chengyzhao/TextPSG)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://vis-www.cs.umass.edu/TextPSG/)

+ [**HiLo: Exploiting high low frequency relations for unbiased panoptic scene graph generation**](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhou_HiLo_Exploiting_High_Low_Frequency_Relations_for_Unbiased_Panoptic_Scene_ICCV_2023_paper.pdf)  [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]() [![Star](https://img.shields.io/github/stars/franciszzj/HiLo.svg?style=social&label=Star)](https://github.com/franciszzj/HiLo)

+ [**Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2207.11247) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]() [![Star](https://img.shields.io/github/stars/Jingkang50/OpenPSG.svg?style=social&label=Star)](https://github.com/Jingkang50/OpenPSG)


+ [**Segmentation-grounded Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Khandelwal_Segmentation-Grounded_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-00CED1)]() [![Star](https://img.shields.io/github/stars/ubc-vision/segmentation-sg.svg?style=social&label=Star)](https://github.com/ubc-vision/segmentation-sg) 




## Spatio-Temporal (Video) Scene Graph Generation

Spatio-Temporal (Video) Scene Graph Generation, a.k.a, dynamic scene graph generation, aims to provide a detailed and structured interpretation of the whole scene by parsing an event into a sequence of interactions between different visual entities. It ususally involves two subtasks:

- `Scene graph detection`: aims to generate scene graphs for given videos, comprising detection results of subject-object pari and the associatde predicates. The localization of object prediction is considered accurate when the Intersection over Union (IoU) between the prediction and ground truth is greater than 0.5.
- `Predicate classification`: classifiy predicates for given oracle detection results of subject-object pairs.
- <details><summary>Noted</summary>Noted: Evaluation is conducted with two settings: ***With Constraint*** and ***No constraints***. In the former the generated graphs are restricted to at most one edge, i.e., each subject-object pair is allowed only one predicate and in the latter, the graphs can have multiple edges</details>


### LLM-based 

+ [**Tri-modal Confluence with Temporal Dynamics for Scene Graph Generation in Operating Rooms**](https://arxiv.org/pdf/2404.09231) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()






### Non-LLM-based


+ [**CYCLO: Cyclic Graph Transformer Approach to Multi-Object Relationship Modeling in Aerial Videos**](https://arxiv.org/pdf/2406.01029) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**OED: Towards One-stage End-to-End Dynamic Scene Graph Generation**](https://arxiv.org/pdf/2405.16925) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/guanw-pku/OED.svg?style=social&label=Star)](https://github.com/guanw-pku/OED) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/oed-cvpr24/%E9%A6%96%E9%A1%B5)

+ [**HIG: Hierarchical Interlacement Graph Approach to Scene Graph Generation in Video Understanding**](https://arxiv.org/pdf/2312.03050) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://uark-cviu.github.io/ASPIRe/) <details><summary>Summary</summary>Introduce a new dataset which delves into interactivities understanding within visual content by deriving scene graph representations from dense interactivities among humans and objects</details>

+ [**Action Scene Graphs for Long-Form Understanding of Egocentric Videos**](https://arxiv.org/pdf/2312.03391) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/fpv-iplab/EASG.svg?style=social&label=Star)](https://github.com/fpv-iplab/EASG)


+ [**End-to-End Video Scene Graph Generation With Temporal Propagation Transformer**](https://ieeexplore.ieee.org/document/10145598) [![Paper](https://img.shields.io/badge/TMM23-556b2f)]()





+ [**Unbiased scene graph generation in videos**](https://openaccess.thecvf.com/content/CVPR2023/papers/Nag_Unbiased_Scene_Graph_Generation_in_Videos_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/sayaknag/unbiasedSGG.svg?style=social&label=Star)](https://github.com/sayaknag/unbiasedSGG)

+ [**Panoptic Video Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Yang_Panoptic_Video_Scene_Graph_Generation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/LilyDaytoy/OpenPVSG.svg?style=social&label=Star)](https://github.com/LilyDaytoy/OpenPVSG)

+ [**Cross-Modality Time-Variant Relation Learning for Generating Dynamic Scene Graphs**](https://arxiv.org/abs/2305.08522) [![Paper](https://img.shields.io/badge/ICRA23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/qncsn2016/TR2.svg?style=social&label=Star)](https://github.com/qncsn2016/TR2)

+ [**Video Scene Graph Generation from Single-Frame Weak Supervision**](https://openreview.net/pdf?id=KLrGlNoxzb4) [![Paper](https://img.shields.io/badge/ICLR23-696969)]() [![Star](https://img.shields.io/github/stars/zjucsq/PLA.svg?style=social&label=Star)](https://github.com/zjucsq/PLA)

+ [**Prior Knowledge-driven Dynamic Scene Graph Generation with Causal Inference**](https://dl.acm.org/doi/10.1145/3581783.3612249)  [![Paper](https://img.shields.io/badge/MM23-8b4513)]()

+ [**Dynamic scene graph generation via temporal prior inference**](https://dl.acm.org/doi/abs/10.1145/3503161.3548324) [![Paper](https://img.shields.io/badge/MM22-8b4513)]()

+ [**VRDFormer: End-to-End Video Visual Relation Detection with Transformers**](https://openaccess.thecvf.com/content/CVPR2022/papers/Zheng_VRDFormer_End-to-End_Video_Visual_Relation_Detection_With_Transformers_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Star](https://img.shields.io/github/stars/zhengsipeng/VRDFormer_VRD.svg?style=social&label=Star)](https://github.com/zhengsipeng/VRDFormer_VRD)


+ [**Dynamic Scene Graph Generation via Anticipatory Pre-training**](https://openaccess.thecvf.com/content/CVPR2022/papers/Li_Dynamic_Scene_Graph_Generation_via_Anticipatory_Pre-Training_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]()

+ [**Meta Spatio-Temporal Debiasing for Video Scene Graph Generation**](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136870368.pdf) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]()

+ [**Spatial-temporal transformer for dynamic scene graph generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Cong_Spatial-Temporal_Transformer_for_Dynamic_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Star](https://img.shields.io/github/stars/yrcong/STTran.svg?style=social&label=Star)](https://github.com/yrcong/STTran)

+ [**Target adaptive context aggregation for video scene graph generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Teng_Target_Adaptive_Context_Aggregation_for_Video_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Star](https://img.shields.io/github/stars/MCG-NJU/TRACE.svg?style=social&label=Star)](https://github.com/MCG-NJU/TRACE)


+ [**Video Visual Relation Detection**](https://dl.acm.org/doi/10.1145/3123266.3123380) [![Paper](https://img.shields.io/badge/MM23-8b4513)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://xdshang.github.io/docs/imagenet-vidvrd.html)






## Audio Scene Graph Generation

+ [**Visual Scene Graphs for Audio Source Separation**](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() 

+ [**Learning Audio-Visual Dynamics Using Scene Graphs for Audio Source Separation**](https://arxiv.org/pdf/2210.16472) [![Paper](https://img.shields.io/badge/NIPS22-CD5C5C2)]() 





## 3D Scene Graph Generation

+ [**EchoScene: Indoor Scene Generation via Information Echo over Scene Graph Diffusion**](https://arxiv.org/pdf/2405.00915) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/ymxlzgy/echoscene.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/echoscene)

+ [**Weakly-Supervised 3D Scene Graph Generation via Visual-Linguistic Assisted Pseudo-labeling**](https://arxiv.org/pdf/2404.02527) [![Paper](https://img.shields.io/badge/arXiv24-b22222)](https://arxiv.org/pdf/2309.15702)  

+ [**SGRec3D: Self-Supervised 3D Scene Graph Learning via Object-Level Scene Reconstruction**](https://arxiv.org/pdf/2309.15702)  [![Paper](https://img.shields.io/badge/WACV24-800080)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://kochsebastian.com/sgrec3d)

+ [**Open3DSG: Open-Vocabulary 3D Scene Graphs from Point Clouds with Queryable Objects and Open-Set Relationships**](https://kochsebastian.com/open3dsg) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/boschresearch/Open3DSG.svg?style=social&label=Star)](https://github.com/boschresearch/Open3DSG) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://kochsebastian.com/open3dsg)

+ [**CLIP-Driven Open-Vocabulary 3D Scene Graph Generation via Cross-Modality Contrastive Learning**](https://openaccess.thecvf.com/content/CVPR2024/papers/Chen_CLIP-Driven_Open-Vocabulary_3D_Scene_Graph_Generation_via_Cross-Modality_Contrastive_Learning_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]()

+ [**Incremental 3D Semantic Scene Graph Prediction from RGB Sequences**](https://openaccess.thecvf.com/content/CVPR2023/papers/Wu_Incremental_3D_Semantic_Scene_Graph_Prediction_From_RGB_Sequences_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://shunchengwu.github.io/MonoSSG)

+ [**SceneGraphFusion: Incremental 3D Scene Graph Prediction from RGB-D Sequences**](https://openaccess.thecvf.com/content/CVPR2021/papers/Wu_SceneGraphFusion_Incremental_3D_Scene_Graph_Prediction_From_RGB-D_Sequences_CVPR_2021_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR21-8A2BE2)]() [![Star](https://img.shields.io/github/stars/ShunChengWu/SceneGraphFusion.svg?style=social&label=Star)](https://github.com/ShunChengWu/SceneGraphFusion) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://shunchengwu.github.io/SceneGraphFusion)

+ [**Learning 3D Semantic Scene Graphs from 3D Indoor Reconstructions**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wald_Learning_3D_Semantic_Scene_Graphs_From_3D_Indoor_Reconstructions_CVPR_2020_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/ShunChengWu/3DSSG.svg?style=social&label=Star)](https://github.com/ShunChengWu/3DSSG) 





## Textual Scene Graph Generation

+ [**FACTUAL: A Benchmark for Faithful and Consistent Textual Scene Graph Parsing**](https://arxiv.org/pdf/2305.17497) [![Paper](https://img.shields.io/badge/ACL23-191970)]()  [![Star](https://img.shields.io/github/stars/zhuang-li/FactualSceneGraph.svg?style=social&label=Star)](https://github.com/zhuang-li/FactualSceneGraph) 

+ [**Scene Graph Parsing via Abstract Meaning Representation in Pre-trained Language Models**](https://aclanthology.org/2022.dlg4nlp-1.4.pdf) [![Paper](https://img.shields.io/badge/DLG4NLP22-deb887)]() 

+ [**Scene Graph Parsing by Attention Graph**](https://arxiv.org/pdf/1909.06273) [![Paper](https://img.shields.io/badge/NIPS18-CD5C5C2)]()

+ [**Scene Graph Parsing as Dependency Parsing**](https://www.cs.jhu.edu/~cxliu/papers/sgparser_naacl18.pdf) [![Paper](https://img.shields.io/badge/NAACL18-191970)]() [![Star](https://img.shields.io/github/stars/Yusics/bist-parser.svg?style=social&label=Star)](https://github.com/Yusics/bist-parser/tree/sgparser) 

+ [**Generating Semantically Precise Scene Graphs from Textual Descriptions for Improved Image Retrieval**](https://nlp.stanford.edu/pubs/schuster-krishna-chang-feifei-manning-vl15.pdf) [![Paper](https://img.shields.io/badge/VL15-191970)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://nlp.stanford.edu/software/scenegraph-parser.shtml)
---




# 🥝 Scene Graph Application




## Image Retrieval

+ [**Cross-modal Scene Graph Matching for Relationship-aware Image-Text Retrieval**](https://openaccess.thecvf.com/content_WACV_2020/papers/Wang_Cross-modal_Scene_Graph_Matching_for_Relationship-aware_Image-Text_Retrieval_WACV_2020_paper.pdf) [![Paper](https://img.shields.io/badge/WACV20-800080)]()


+ [**Image Retrieval using Scene Graphs**](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR15-8A2BE2)]()







## 2D Image Generation

+ [**SG-Adapter: Enhancing Text-to-Image Generation with Scene Graph Guidance**](https://arxiv.org/pdf/2405.15321) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Generated Contents Enrichment**](https://arxiv.org/pdf/2405.03650) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

## Visual Question Answering 
+ [**SOK-Bench: A Situated Video Reasoning Benchmark with Aligned Open-World Knowledge**](https://arxiv.org/pdf/2405.09713) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://bobbywu.com/SOKBench/)


## Enhanced VLM/MLLM

+ [**Compositional Chain-of-Thought Prompting for Large Multimodal Models**](https://arxiv.org/pdf/2311.17076) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/chancharikmitra/CCoT.svg?style=social&label=Star)](https://github.com/chancharikmitra/CCoT)


+ [**The All-Seeing Project V2: Towards General Relation Comprehension of the Open World**](https://arxiv.org/pdf/2402.19474) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/OpenGVLab/all-seeing.svg?style=social&label=Star)](https://github.com/OpenGVLab/all-seeing) <details><summary>New dataset and New Task (Relation Conversation) </summary>we propose a novel task, termed Relation Conversation (ReC), which unifies the formulation of text generation, object localization, and relation comprehension. Based on the unified formulation, we construct the AS-V2 dataset, which consists of 127K high-quality relation conversation samples, to unlock the ReC capability for Multi-modal Large Language Models (MLLMs).</details>


+ [**The All-Seeing Project: Towards Panoptic Visual Recognition and Understanding of the Open World**](https://arxiv.org/pdf/2308.01907) [![Paper](https://img.shields.io/badge/NIPS23-CD5C5C)]() <details><summary>New dataset and a unified vision-language model for open-word panoptic visual recognition and understanding</summary>we propose a new large-scale dataset (AS-1B) for open-world panoptic visual recognition and understanding, using an economical semi-automatic data engine that combines the power of off-the-shelf vision/language models and human feedback. Moreover,  we develop a unified vision-language foundation model (ASM) for open-world panoptic visual recognition and understanding. Aligning with LLMs, our ASM supports versatile image-text retrieval and generation tasks, demonstrating impressive zero-shot capability.</details>

+ [**Cross-modal Attention Congruence Regularization for Vision-Language Relation Alignment**](https://aclanthology.org/2023.acl-long.298.pdf) [![Paper](https://img.shields.io/badge/ACL23-191970)]() 


+ [**Incorporating Structured Representations into Pretrained Vision & Language Models Using Scene Graphs**](https://aclanthology.org/2023.emnlp-main.870.pdf) [![Paper](https://img.shields.io/badge/EMNLP23-191970)]()

+ [**Fine-Grained Semantically Aligned Vision-Language Pre-Training**](https://arxiv.org/pdf/2208.02515) [![Paper](https://img.shields.io/badge/NIPS22-CD5C5C)]() [![Star](https://img.shields.io/github/stars/YYJMJC/LOUPE.svg?style=social&label=Star)](https://github.com/YYJMJC/LOUPE)

+ [**ERNIE-ViL: Knowledge Enhanced Vision-Language Representations through Scene Graphs**](https://arxiv.org/pdf/2006.16934) [![Paper](https://img.shields.io/badge/AAAI21-191970)]()  [![Star](https://img.shields.io/github/stars/zhuang-li/FactualSceneGraph.svg?style=social&label=Star)](https://github.com/zhuang-li/FactualSceneGraph) 





## Information Extraction

+ [**M3S: Scene Graph Driven Multi-Granularity Multi-Task Learning for Multi-Modal NER**](https://ieeexplore.ieee.org/abstract/document/9944151) [![Paper](https://img.shields.io/badge/TPAMI-ffa07a)]()

## 3D Generation

+ [**Compositional 3D Scene Synthesis with Scene Graph Guided Layout-Shape Generation**](https://arxiv.org/pdf/2403.12848) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**GraphDreamer: Compositional 3D Scene Synthesis from Scene Graphs**](https://arxiv.org/pdf/2312.00093)  [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/GGGHSL/GraphDreamer.svg?style=social&label=Star)](https://github.com/GGGHSL/GraphDreamer) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://graphdreamer.github.io/)





## Mitigate Hallucination 

+ [**BACON: Supercharge Your VLM with Bag-of-Concept Graph to Mitigate Hallucinations**](https://arxiv.org/pdf/2407.03314) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/ztyang23/BACON.svg?style=social&label=Star)](https://github.com/ztyang23/BACON) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://ztyang23.github.io/bacon-page/)

+ [**Mitigating Hallucination in Visual Language Models with Visual Supervision**](https://arxiv.org/pdf/2311.16479) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() 



## Dynamic Environment Guidance

+ [**Situational Instructions Database: Task Guidance in Dynamic Environments**](https://arxiv.org/pdf/2406.13302) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/mindgarage/situational-instructions-database.svg?style=social&label=Star)](https://github.com/mindgarage/situational-instructions-database)

+ [**RoboHop: Segment-based Topological Map Representation for Open-World Visual Navigation**](https://arxiv.org/pdf/2405.05792) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://oravus.github.io/RoboHop/)

+ [**LLM-Personalize: Aligning LLM Planners with Human Preferences via Reinforced Self-Training for Housekeeping Robots**]() [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/donggehan/codellmpersonalize.svg?style=social&label=Star)](https://github.com/donggehan/codellmpersonalize) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://donggehan.github.io/projectllmpersonalize/)



## Privacy-sensitive Object Identification

+ [**Beyond Visual Appearances: Privacy-sensitive Objects Identification via Hybrid Graph Reasoning**](https://arxiv.org/pdf/2406.12736) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


## Referring Expression Comprehension

+ [**Zero-shot Referring Expression Comprehension via Structural Similarity Between Images and Captions**](https://openaccess.thecvf.com/content/CVPR2024/papers/Han_Zero-shot_Referring_Expression_Comprehension_via_Structural_Similarity_Between_Images_and_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/Show-han/Zeroshot_REC.svg?style=social&label=Star)](https://github.com/Show-han/Zeroshot_REC) <details><summary>A triplet-matching objective to fine-tune the vision-language alignment models.</summary>To mitigate this gap, we leverage large foundation models to disentangle both images and texts into triplets in the format of (subject, predicate, object). After that, grounding is accomplished by calculating the structural similarity matrix between visual and textual triplets with a VLA model, and subsequently propagate it to an instancelevel similarity matrix. Furthermore, to equip VLA models with the ability of relationship nderstanding, we design a triplet-matching objective to fine-tune the VLA models on a collection of curated dataset containing abundant entity relationships</details>



## Video Retrieval


+ [**A Review and Efficient Implementation of Scene Graph Generation Metricsl**](https://arxiv.org/pdf/2404.09616) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/lorjul/sgbench.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://lorjul.github.io/sgbench/)



---


# 🤶 Evaluation Metrics

+ [**A Review and Efficient Implementation of Scene Graph Generation Metrics**](https://arxiv.org/pdf/2404.09616) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/lorjul/sgbench.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://lorjul.github.io/sgbench/)

+ [**Semantic Similarity Score for Measuring Visual Similarity at Semantic Level**](https://arxiv.org/pdf/2406.03865) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() <details>Sumarry</details>


---

# 🐱‍🚀 Miscellaneous

## Toolkit
Here, we provide some toolkits for parsing scene graphs or other useful tools for referencess.


+ [**Stanford Scene Graph Parser**](https://nlp.stanford.edu/software/scenegraph-parser.shtml)

+ [**SceneGraphParser**](https://github.com/vacancy/SceneGraphParser) [![Star](https://img.shields.io/github/stars/vacancy/SceneGraphParser.svg?style=social&label=Star)](https://github.com/vacancy/SceneGraphParser)


## Workshop

+ [**2nd Workshop on Scene Graphs and Graph Representation Learning**](https://sites.google.com/view/sg2rl/index) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![YouTube](https://badges.aleen42.com/src/youtube.svg)](https://www.youtube.com/watch?v=qvof1eiN-E0)

+ [**First ICCV Workshop on Scene Graphs and Graph Representation Learning**](https://sites.google.com/view/sg2rl/sg2rl-2023/home) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]() [[paper_list]](https://github.com/DmitryRyumin/ICCV-2023-Papers/blob/main/sections/2023/workshops/w-scene-graphs-and-graph-representation-learning.md)


+ [**Scene Graph Representation and Learning**](https://cs.stanford.edu/people/ranjaykrishna/sgrl/index.html) [![Paper](https://img.shields.io/badge/ICCV19-2f4f4f)]() 

+ [**DIRA Workshop and Challenge**](https://cvpr-dira.lipingyang.org/) 

+ [**Lecture 18: Scene Graphs and Graph Convolutions**](https://cs231n.stanford.edu/slides/2020/lecture_18.pdf)


## Survey

+ [**Scene Graphs: A Survey of Generations and Applications**](https://www.xiaojun.ai/papers/Scene-Graph-Survey.pdf)

+ [**Scene Graph Generation: A Comprehensive Survey**](https://arxiv.org/pdf/2201.00443)


## Insteresting Works

+ [**Visually Grounded Concept Composition**](https://arxiv.org/pdf/2109.14115)
+ [**AIMS: All-Inclusive Multi-Level Segmentation for Anything**](https://proceedings.neurips.cc/paper_files/paper/2023/file/3da292ced54290c19fc55d9dba3da793-Paper-Conference.pdf)



# ⭐️ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=ChocoWu/Awesome-Scene-Graph-for-VL-Learning&type=Date)](https://star-history.com/#ChocoWu/Awesome-Scene-Graph-for-VL-Learning&Date)
