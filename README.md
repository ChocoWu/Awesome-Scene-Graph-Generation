<div align="center">
<h1> Awesome-Scene-Graph-Generation </h1> 
</div>


# 📣 News
- ✨✨✨We are organizing a **WACV26 Workshop** on [Scene Graph for Structured Intelligence](https://scene-graph.github.io/SG4SI-WACV26/), welcome submission.


- We're excited to introduce a new section:🔥 Hot Topics 🔥!

  We'll regularly post interesting discussion topics in the Issues tab. If you're interested, feel free to jump in and share your thoughts! These discussions are purely for idea exchange and community engagement 

  I'll also be collecting and sharing thought-provoking questions related to the future of scene graphs and scene understanding in general. Everyone is welcome to join the conversation!

## 🔍 First Topic:
- [**"Are scene graphs still a good way to represent and understand scenes?"**](https://github.com/ChocoWu/Awesome-Scene-Graph-Generation/issues/7)
  
  Scene graphs are a form of explicit scene representation. But with the rise of implicit scene representations, is this approach still effective? Which representation is more promising moving forward?

- [**Can we define the scene-level for a scene graph?**](https://github.com/ChocoWu/Awesome-Scene-Graph-Generation/issues/12)

Let us know what you think in the [discussion thread](https://github.com/ChocoWu/Awesome-Scene-Graph-Generation/issues/7)!




# 🎨 Introduction 
A scene graph is a topological structure representing a scene described in text, image, video, or etc. 
In this graph, the nodes correspond to object bounding boxes with their category labels and attributes, while the edges represent the pair-wise relationships between objects. 
  <p align="center">
  <img src="assets/intro1.png" width="75%">
</p>

---

# 📕 Table of Contents
- [🌷 Scene Graph Datasets](#-datasets)
- [🍕 Scene Graph Generation](#-scene-graph-generation)
  - [2D (Image) Scene Graph Generation](#2d-image-scene-graph-generation)
  - [Panoptic Scene Graph Generation](#panoptic-scene-graph-generation)
  - [Spatio-Temporal (Video) Scene Graph Generation](#spatio-temporal-video-scene-graph-generation)
  - [Audio Scene Graph Generation](#audio-scene-graph-generation)
  - [3D Scene Graph Generation](#3d-scene-graph-generation)
  - [4D Scene Graph Gnereation](#4d-scene-graph-gnereation)
  - [Textual Scene Graph Generation](#textual-scene-graph-generation)
  - [Map Space Scene Graph](#map-space-scene-graph)
  - [Universal Scene Graph Generation](#universal-scene-graph-generation)
- [🥝 Scene Graph Application](#-scene-graph-application)
  - [Image Retrieval](#image-retrieval)
  - [Image/Video Caption](#imagevideo-caption)
  - [2D Image Generation](#2d-image-generation)
  - [2D/Video Visual Reasoning](#2dvideo-scene-visual-reasoning)
  - [3D Visual Scene Reasoning](#3d-scene-visual-reasoning)
  - [VLM/MLLM Enhancing](#enhanced-vlmmllm)
  - [Information Extraction](#information-extraction)
  - [3D Scene Generation](#3d-scene-generation)
  - [Mitigate Hallucination](#mitigate-hallucination)
  - [Dynamic Environment Guidance](#dynamic-environment-guidance)
  - [Privacy-sensitive Object Identification](#privacy-sensitive-object-identification)
  - [Referring Expression Comprehension](#referring-expression-comprehension)
  - [Video Retrieval](#video-retrieval)
- [🤶 Evaluation Metrics](#evaluation-metrics)
- [🐱‍🚀 Miscellaneous](#miscellaneous)
  - [Toolkit](#toolkit)
  - [Workshop](#workshop)
  - [Survey](#survey)
  - [Insteresting Works](#insteresting-works)
- [⭐️ Star History](#️-star-history)


---


# 🌷 Scene Graph Datasets
<p align="center">

| Dataset |  Modality  |   Obj. Class  | BBox | Rela. Class | Triplets | Instances | 
|:--------:|:--------:|:--------:| :--------:|  :--------:|  :--------:|  :--------:|
| [ReplicaSGG](https://github.com/Howardkhh/ReplicaSSG) | Image, 3D | 34 | - | 8 | - | - |
| [Visual Phrase](https://vision.cs.uiuc.edu/phrasal/) | Image | 8 | 3,271 | 9 | 1,796 | 2,769 |
| [Scene Graph](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) | Image | 266 | 69,009 | 68 | 109,535 | 5,000 |
| [VRD](https://cs.stanford.edu/people/ranjaykrishna/vrd/)  | Image | 100 | - | 70 | 37,993 | 5,000 |
| [Open Images v7](https://storage.googleapis.com/openimages/web/index.html)  | Image | 600 | 3,290,070 | 31 | 374,768 | 9,178,275 |
| [Visual Genome](https://homes.cs.washington.edu/~ranjay/visualgenome/index.html) | Image | 5,996 | 3,843,636 | 1,014 | 2,347,187 | 108,077 | 
| [GQA](https://cs.stanford.edu/people/dorarad/gqa/about.html) | Image | 200 | - | 310 | - | 3,795,907 | 74,942 |
| [VrR-VG](http://vrrvg.com/) | Image | 1,600 | 282,460 | 117 | 203,375 | 58,983 |
| [UnRel](https://www.di.ens.fr/willow/research/unrel/) | Image | - | - | 18 | 76 |  1,071 |
| [SpatialSense](https://github.com/princeton-vl/SpatialSense) | Image | 3,679 | - | 9 | 13,229 | 11,569 |
| [SpatialVOC2K](https://github.com/muskata/SpatialVOC2K) | Image | 20 | 5,775 | 34 | 9,804 | 2,026 | 
| [OpenSG](https://github.com/Jingkang50/OpenPSG) | Image (panoptic) | 133 | - | 56 | - | 49K |
| [AUG](https://arxiv.org/pdf/2404.07788) | Image (Overhead View) | 76 | - | 61 | - | - |
| [STAR](https://arxiv.org/pdf/2406.09410) | Satellite Imagery | 48 | 219,120 | 58 | 400,795 | 31,096 |
| [ReCon1M](https://arxiv.org/pdf/2406.06028) | Satellite Imagery | 60 |  859,751 | 64 | 1,149,342 |  21,392 |
| [SkySenseGPT](https://github.com/Luo-Z13/SkySenseGPT) | Satellite Imagery (Instruction) | - | - | - | - | - |
| [Traffic Scene Graph](https://ieeexplore.ieee.org/abstract/document/9900075) | Traffic Image| 2，266 | - | 4,272 | - | 451 |
| [ImageNet-VidVRD](https://xdshang.github.io/docs/imagenet-vidvrd.html) | Video | 35 | - | 132 | 3,219 | 100 |
| [VidOR](https://xdshang.github.io/docs/vidor.html) | Video | 80 | - | 50 | - | 10,000 |
| [Action Genome](https://github.com/JingweiJ/ActionGenome) | Video | 35 | 0.4M | 25 | 1.7M | 10,000 |
| [AeroEye](https://arxiv.org/pdf/2406.01029) | Video (Drone-View) | 56 | - | 384 | - | 2.2M |
| [PVSG](https://jingkang50.github.io/PVSG/) | Video (panoptic) | 126 | - |  57 |  4,587 | 400|
| [ASPIRe](https://uark-cviu.github.io/ASPIRe/) | Video(Interlacements) | - | - | 4.5K | - | 1.5K |
| [Ego-EASG](https://github.com/fpv-iplab/EASG) | Video(Ego-view) | 407 | - | 235 | - | - |
| [3D Semantic Scene Graphs (3DSSG)](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wald_Learning_3D_Semantic_Scene_Graphs_From_3D_Indoor_Reconstructions_CVPR_2020_paper.pdf) | 3D | 528 | - | 39 | - | 48K|
| [PSG4D](https://arxiv.org/pdf/2405.10305) | 4D | 46 | - | 15 | - | - | - |
| [4D-OR](https://github.com/egeozsoy/4D-OR) | 4D(operating room) | 12 | - | 14 | - | - |
| [MM-OR](https://github.com/egeozsoy/MM-OR) | 4D(operating room) | - | - | - | - | - |
| [EgoExOR](https://github.com/egeozsoy/4D-OR) | 4D(operating room) | 36 | - | 22 | 568,235 | - |
| [FACTUAL](https://github.com/zhuang-li/FactualSceneGraph) |  Image, Text  | 4,042 | - | 1,607 | 40,149 | 40,369 |
| [TSG Bench](https://tsg-bench.netlify.app/) |  Text  | - | - | - | 11,820 | 4,289 |
| [DiscoSG-DS](https://github.com/ShaoqLin/DiscoSG) |  Image, Text  | 4,018 | - | 2,033 | 68,478 | 8,830 |
| [Open-set Scene Graph](https://github.com/MotoharuSonogashira/open-set-scene-graph-dataset) |  Image  | 150 | - | 50 | - | - |
</p>


## Toolkit
Here, we provide some toolkits for parsing scene graphs or other useful tools for referencess.


+ [**Stanford Scene Graph Parser**](https://nlp.stanford.edu/software/scenegraph-parser.shtml)

+ [**SceneGraphParser**](https://github.com/vacancy/SceneGraphParser) [![Star](https://img.shields.io/github/stars/vacancy/SceneGraphParser.svg?style=social&label=Star)](https://github.com/vacancy/SceneGraphParser)

+ [**FactualSceneGraph**](https://github.com/zhuang-li/FactualSceneGraph) [![Star](https://img.shields.io/github/stars/zhuang-li/FactualSceneGraph.svg?style=social&label=Star)](https://github.com/zhuang-li/FactualSceneGraph)

+ [**Scene-Graph-Benchmark.pytorch**](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch)  [![Star](https://img.shields.io/github/stars/KaihuaTang/Scene-Graph-Benchmark.pytorch.svg?style=social&label=Star)](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch)

+ [**SGG-Benchmark🙆‍♀️👈**](https://github.com/Maelic/SGG-Benchmark)  [![Star](https://img.shields.io/github/stars/Maelic/SGG-Benchmark.svg?style=social&label=Star)](https://github.com/Maelic/SGG-Benchmark)
  <details><summary>A new benchmark for the task of Scene Graph Generation</summary>This new codebase provides an up-to-date and easy-to-run implementation of common approaches in the filed of Scene Graph Generation. Welcome to have a try and contribute to this codebase.</details>

+ [**SGG-Annotate**](https://github.com/Maelic/SGG-Annotate) [![Star](https://img.shields.io/github/stars/Maelic/SGG-Annotate.svg?style=social&label=Star)](https://github.com/Maelic/SGG-Annotate)
  <details><summary>Scene Graph Annotation tool</summary>A modern annotation tool for annotating visual relationships in COCO format.</details>
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


+ [**Compile Scene Graphs with Reinforcement Learning**](https://arxiv.org/pdf/2504.13617) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()  [![Star](https://img.shields.io/github/stars/gpt4vision/R1-SGG.svg?style=social&label=Star)](https://github.com/gpt4vision/R1-SGG) 
  <details><summary>R1-based model</summary> R1-SGG, a novel framework leveraging visual instruction tuning enhanced by reinforcement learning (RL). The visual instruction tuning stage follows a conventional supervised fine-tuning (SFT) paradigm, i.e., finetuning the model using prompt-response pairs with a cross-entropy loss. For the RL stage, we adopt GRPO, an online policy optimization algorithm, in which an node-level reward and edge-level reward are designed.</details>


+ [**Hallucinate, Ground, Repeat: A Framework for Generalized Visual Relationship Detection**](https://arxiv.org/pdf/2506.05651) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 

+ [**PRISM-0: A Predicate-Rich Scene Graph Generation Framework for Zero-Shot Open-Vocabulary Tasks**](https://arxiv.org/pdf/2504.00844) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 


+ [**From Data to Modeling: Fully Open-vocabulary Scene Graph Generation**](https://arxiv.org/pdf/2505.20106) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()    [![Star](https://img.shields.io/github/stars/gpt4vision/OvSGTR.svg?style=social&label=Star)](https://github.com/gpt4vision/OvSGTR) 

+ [**Open World Scene Graph Generation using Vision Language Models**](https://arxiv.org/pdf/2506.08189) [![Paper](https://img.shields.io/badge/CVPR25W-8A2BE2)]() 

+ [**Synthetic Visual Genome**](https://www.arxiv.org/pdf/2506.07643) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() [![Star](https://img.shields.io/github/stars/jamespark3922/SyntheticVG.svg?style=social&label=Star)](https://github.com/jamespark3922/SyntheticVG)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://synthetic-visual-genome.github.io/)

+ [**Conformal Prediction and MLLM aided Uncertainty Quantification in Scene Graph Generation**](https://arxiv.org/pdf/2503.13947) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() 


+ [**LLaVA-SpaceSGG: Visual Instruct Tuning for Open-vocabulary Scene Graph Generation with Enhanced Spatial Relations**](https://arxiv.org/pdf/2412.06322) [![Paper](https://img.shields.io/badge/WACV24-6a5acd)]()  [![Star](https://img.shields.io/github/stars/Endlinc/LLaVA-SpaceSGG.svg?style=social&label=Star)](https://github.com/Endlinc/LLaVA-SpaceSGG) 

+ [**Tri-modal Confluence with Temporal Dynamics for Scene Graph Generation in Operating Rooms**](https://arxiv.org/pdf/2404.09231) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() 


+ [**Scene Graph Generation Strategy with Co-occurrence Knowledge and Learnable Term Frequency**](https://arxiv.org/pdf/2405.12648) [![Paper](https://img.shields.io/badge/ICML24-FF7F50)]() 


+ [**Scene Graph Generation with Role-Playing Large Language Models**](https://arxiv.org/pdf/2410.15364) [![Paper](https://img.shields.io/badge/NIPS24-CD5C5C)]() 

+ [**SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding**](https://arxiv.org/pdf/2406.10100) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Luo-Z13/SkySenseGPT.svg?style=social&label=Star)](https://github.com/Luo-Z13/SkySenseGPT) 

+ [**VLPrompt: Vision-Language Prompting for Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2311.16492) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/franciszzj/VLPrompt.svg?style=social&label=Star)](https://github.com/franciszzj/VLPrompt) 

+ [**SceneLLM: Implicit Language Reasoning in LLM for Dynamic Scene Graph Generation**](https://arxiv.org/pdf/2412.11026) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**From Pixels to Graphs: Open-Vocabulary Scene Graph Generation with Vision-Language Models**](https://arxiv.org/pdf/2404.00906) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/SHTUPLUS/Pix2Grp_CVPR2024.svg?style=social&label=Star)](https://github.com/SHTUPLUS/Pix2Grp_CVPR2024) 

+ [**LLM4SGG: Large Language Models for Weakly Supervised Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2024/papers/Kim_LLM4SGG_Large_Language_Models_for_Weakly_Supervised_Scene_Graph_Generation_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/rlqja1107/torch-LLM4SGG.svg?style=social&label=Star)](https://github.com/rlqja1107/torch-LLM4SGG) 

+ [**Visually-Prompted Language Model for Fine-Grained Scene Graph Generation in an Open World**](https://openaccess.thecvf.com/content/ICCV2023/papers/Yu_Visually-Prompted_Language_Model_for_Fine-Grained_Scene_Graph_Generation_in_an_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]()  [![Star](https://img.shields.io/github/stars/Yuqifan1117/CaCao.svg?style=social&label=Star)](https://github.com/Yuqifan1117/CaCao) 


+ [**GPT4SGG: Synthesizing Scene Graphs from Holistic and Region-specific Narratives**](https://arxiv.org/pdf/2312.04314) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://gpt4vision.github.io/gpt4sgg/)


+ [**Less is More: Toward Zero-Shot Local Scene Graph Generation via Foundation Models**](https://arxiv.org/pdf/2310.01356)  [![Paper](https://img.shields.io/badge/arXiv23-b22222)]()


+ [**Enhancing Scene Graph Generation with Hierarchical Relationships and Commonsense Knowledge**](https://arxiv.org/pdf/2311.12889) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() [![Star](https://img.shields.io/github/stars/bowen-upenn/scene_graph_commonsense.svg?style=social&label=Star)](https://github.com/bowen-upenn/scene_graph_commonsense) 🙆‍♀️👈 


### Non-LLM-based

+ [**Vision-Language Interactive Relation Mining for Open-Vocabulary Scene Graph Generation**](https://iccv.thecvf.com/virtual/2025/poster/267)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]() 


+ [**Hybrid Reciprocal Transformer with Triplet Feature Alignment for Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2025/papers/Fu_Hybrid_Reciprocal_Transformer_with_Triplet_Feature_Alignment_for_Scene_Graph_CVPR_2025_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://hq-sg.github.io/)

+ [**Navigating the Unseen: Zero-shot Scene Graph Generation via Capsule-Based Equivariant Features**](https://openaccess.thecvf.com/content/CVPR2025/papers/Huang_Navigating_the_Unseen_Zero-shot_Scene_Graph_Generation_via_Capsule-Based_Equivariant_CVPR_2025_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()

+ [**A Reverse Causal Framework to Mitigate Spurious Correlations for Debiasing Scene Graph Generation**](https://arxiv.org/pdf/2505.23451) [![Paper](https://img.shields.io/badge/TPAMI25-ffa07a)]()


+ [**CoPa-SG: Dense Scene Graphs with Parametric and Proto-Relations**](https://arxiv.org/pdf/2506.21357) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()
  <details><summary>Introduce the concept of parametric relations</summary>To eliminate ambiguous predicate definitions, we introduce the concept of <b>parametric relations</b>. In addition to a traditional predicate label, we store a <b>parameter</b> (e.g. an angle or a distance) that enables a more fine-grained representation. We show how existing models can be adapted to the new parametric scene graph generation task. Additionally, we introduce <b>proto-relations</b> as a novel technique for representing hypothetical relations. Given an anchor object and a predicate, a proto-relation describes the volume or area that another object would need to intersect to fulfill the associated relation with the anchor object. Protorelations can encode information such as "somewhere next to the TV" or "the area behind the sofa". This representation will arguably be useful for agents that use scene graphs as their intermediate knowledge state.</details>

+ [**HOIverse: A Synthetic Scene Graph Dataset With Human Object Interactions**](https://arxiv.org/pdf/2506.19639) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://mrunmaivp.github.io/hoiverse/)

+ [**Generalized Visual Relation Detection with Diffusion Models**](https://arxiv.org/pdf/2504.12100) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Robo-SGG: Exploiting Layout-Oriented Normalization and Restitution for Robust Scene Graph Generation**](https://arxiv.org/pdf/2504.12606) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Taking A Closer Look at Interacting Objects: Interaction-Aware Open Vocabulary Scene Graph Generation**](https://arxiv.org/pdf/2502.03856)  [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()


+ [**Relation-aware Hierarchical Prompt for Open-vocabulary Scene Graph Generation**](https://arxiv.org/pdf/2412.19021) [![Paper](https://img.shields.io/badge/AAAI25-c71585)]()

+ [**RA-SGG: Retrieval-Augmented Scene Graph Generation Framework via Multi-Prototype Learning**](https://arxiv.org/pdf/2412.12788)  [![Paper](https://img.shields.io/badge/AAAI25-c71585)]() [![Star](https://img.shields.io/github/stars/KanghoonYoon/torch-rasgg.svg?style=social&label=Star)](https://github.com/KanghoonYoon/torch-rasgg)

+ [**Taking A Closer Look at Interacting Objects: Interaction-Aware Open Vocabulary Scene Graph Generation**](https://arxiv.org/pdf/2502.03856)  [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**UniQ: Unified Decoder with Task-specific Queries for Efficient Scene Graph Generation**](https://arxiv.org/pdf/2501.05687)  [![Paper](https://img.shields.io/badge/MM24-8b4513)]()


+ [**Multiview Scene Graph**](https://arxiv.org/pdf/2410.11187v1)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/ai4ce/MSG.svg?style=social&label=Star)](https://github.com/ai4ce/MSG) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://ai4ce.github.io/MSG/)

+ [**Scene-Graph ViT: End-to-End Open-Vocabulary Visual Relationship Detection**](https://arxiv.org/pdf/2403.14270)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() 


+ [**Fine-Grained Scene Graph Generation via Sample-Level Bias Prediction**](https://arxiv.org/pdf/2407.19259) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Zhuzi24/SBG.svg?style=social&label=Star)](https://github.com/Zhuzi24/SBG)


+ [**REACT: Real-time Efficiency and Accuracy Compromise for Tradeoffs in Scene Graph Generation**](https://arxiv.org/pdf/2405.16116)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Maelic/SGG-Benchmark.svg?style=social&label=Star)](https://github.com/Maelic/SGG-Benchmark)

+ [**BCTR: Bidirectional Conditioning Transformer for Scene Graph Generation**](https://arxiv.org/pdf/2407.18715)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() 


+ [**Hydra-SGG: Hybrid Relation Assignment for One-stage Scene Graph Generation**](https://arxiv.org/pdf/2409.10262) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() 

+ [**Relationship-Aware Unknown Object Detection for Open-Set Scene Graph Generation**](https://ieeexplore.ieee.org/document/10654281)

+ [**Adaptive Self-training Framework for Fine-grained Scene Graph Generation**](https://arxiv.org/pdf/2401.09786) [![Paper](https://img.shields.io/badge/ICLR24-696969)]() [![Star](https://img.shields.io/github/stars/rlqja1107/torch-ST-SGG.svg?style=social&label=Star)](https://github.com/rlqja1107/torch-ST-SGG)

+ [**Scene Graph Generation Strategy with Co-occurrence Knowledge and Learnable Term Frequency**](https://arxiv.org/pdf/2405.12648) [![Paper](https://img.shields.io/badge/ICML24-FF7F50)]()

+ [**Expanding Scene Graph Boundaries: Fully Open-vocabulary Scene Graph Generation via Visual-Concept Alignment and Retention**](https://arxiv.org/pdf/2311.10988) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/gpt4vision/OvSGTR.svg?style=social&label=Star)](https://github.com/gpt4vision/OvSGTR/)


+ [**Semantic Diversity-aware Prototype-based Learning for Unbiased Scene Graph Generation**](https://arxiv.org/pdf/2407.15396) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/JeonJaeHyeong/DPL.svg?style=social&label=Star)](https://github.com/JeonJaeHyeong/DPL)

+ [**Fine-Grained Scene Graph Generation via Sample-Level Bias Prediction**](https://arxiv.org/pdf/2407.19259) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]()

+ [**Multi-Granularity Sparse Relationship Matrix Prediction Network for End-to-End Scene Graph Generation**](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/10738.pdf) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]()

+ [**Groupwise Query Specialization and Quality-Aware Multi-Assignment for Transformer-based Visual Relationship Detection**](https://openaccess.thecvf.com/content/CVPR2024/papers/Kim_Groupwise_Query_Specialization_and_Quality-Aware_Multi-Assignment_for_Transformer-based_Visual_Relationship_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/mlvlab/SpeaQ.svg?style=social&label=Star)](https://github.com/mlvlab/SpeaQ) 

+ [**Leveraging Predicate and Triplet Learning for Scene Graph Generation**](https://arxiv.org/pdf/2406.02038) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/jkli1998/DRM.svg?style=social&label=Star)](https://github.com/jkli1998/DRM) 
 

+ [**DSGG: Dense Relation Transformer for an End-to-end Scene Graph Generation**](https://arxiv.org/pdf/2403.14886) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/zeeshanhayder/DSGG.svg?style=social&label=Star)](https://github.com/zeeshanhayder/DSGGM) 

+ [**HiKER-SGG: Hierarchical Knowledge Enhanced Robust Scene Graph Generation**](https://arxiv.org/pdf/2403.12033) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/zhangce01/HiKER-SGG.svg?style=social&label=Star)](https://github.com/zhangce01/HiKER-SGG)


+ [**EGTR: Extracting Graph from Transformer for Scene Graph Generation**](https://arxiv.org/pdf/2404.02072) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/naver-ai/egtr.svg?style=social&label=Star)](https://github.com/naver-ai/egtr) 

+ [**Generalized Visual Relation Detection with Diffusion Models**](https://arxiv.org/pdf/2504.12100) [![Paper](https://img.shields.io/badge/TCSVT24-6A8428)]()

+ [**STAR: A First-Ever Dataset and A Large-Scale Benchmark for Scene Graph Generation in Large-Size Satellite Imagery**](https://arxiv.org/pdf/2406.09410) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/Zhuzi24/SGG-ToolKit.svg?style=social&label=Star)](https://github.com/Zhuzi24/SGG-ToolKit) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://linlin-dev.github.io/project/STAR)

+ [**Improving Scene Graph Generation with Relation Words’ Debiasing in Vision-Language Models**](https://arxiv.org/pdf/2403.16184) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**Adaptive Visual Scene Understanding: Incremental Scene Graph Generation**](https://arxiv.org/pdf/2310.01636)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Ensemble Predicate Decoding for Unbiased Scene Graph Generation**](https://arxiv.org/pdf/2408.14187)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**ReCon1M:A Large-scale Benchmark Dataset for Relation Comprehension in Remote Sensing Imagery**](https://arxiv.org/pdf/2406.06028) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**RepSGG: Novel Representations of Entities and Relationships for Scene Graph Generation**](https://ieeexplore.ieee.org/document/10531674)  [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Hierarchical Relationships: A New Perspective to Enhance Scene Graph Generation**](https://arxiv.org/pdf/2303.06842)  [![Paper](https://img.shields.io/badge/TPAMI24-ffa07a)]()

+ [**Improving Scene Graph Generation with Superpixel-Based Interaction Learning**](https://dl.acm.org/doi/pdf/10.1145/3581783.3611889) [![Paper](https://img.shields.io/badge/MM23-8b4513)]()


+ [**Reltr: Relation transformer for scene graph generation**](https://arxiv.org/abs/2201.11460) [![Paper](https://img.shields.io/badge/TPAMI23-ffa07a)]()  [![Star](https://img.shields.io/github/stars/yrcong/RelTR.svg?style=social&label=Star)](https://github.com/yrcong/RelTR)

+ [**Unbiased Scene Graph Generation via Two-stage Causal Modeling**](https://arxiv.org/pdf/2307.05276) [![Paper](https://img.shields.io/badge/TPAMI23-ffa07a)]()

+ [**Zero-Shot Scene Graph Generation via Triplet Calibration and Reduction**](https://arxiv.org/pdf/2309.03542) [![Paper](https://img.shields.io/badge/TOMM23-ffa07a)]() [![Star](https://img.shields.io/github/stars/jkli1998/T-CAR.svg?style=social&label=Star)](https://github.com/jkli1998/T-CAR) 

+ [**Evidential Unvertainty and Diversity Guided Active Learning for Scene Graph Generation**](https://openreview.net/pdf?id=xI1ZTtVOtlz) [![Paper](https://img.shields.io/badge/ICLR23-696969)]()

+ [**Prototype-based Embedding Network for Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Zheng_Prototype-Based_Embedding_Network_for_Scene_Graph_Generation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/VL-Group/PENET.svg?style=social&label=Star)]([VL-Group/PENET](https://github.com/VL-Group/PENET))

+ [**IS-GGT: Iterative Scene Graph Generation With Generative Transformers**](https://openaccess.thecvf.com/content/CVPR2023/papers/Kundu_IS-GGT_Iterative_Scene_Graph_Generation_With_Generative_Transformers_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]()


+ [**Learning to Generate Language-supervised and Open-vocabulary Scene Graph using Pre-trained Visual-Semantic Space**](https://openaccess.thecvf.com/content/CVPR2023/papers/Zhang_Learning_To_Generate_Language-Supervised_and_Open-Vocabulary_Scene_Graph_Using_Pre-Trained_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() 

+ [**Fast Contextual Scene Graph Generation with Unbiased Context Augmentation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Jin_Fast_Contextual_Scene_Graph_Generation_With_Unbiased_Context_Augmentation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() 


+ [**Devil’s on the Edges: Selective Quad Attention for Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Jin_Fast_Contextual_Scene_Graph_Generation_With_Unbiased_Context_Augmentation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/hesedjds/SQUAT.svg?style=social&label=Star)](https://github.com/hesedjds/SQUAT)

+ [**Fine-Grained is Too Coarse: A Novel Data-Centric Approach for Efficient Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2023W/SG2RL/papers/Neau_Fine-Grained_is_Too_Coarse_A_Novel_Data-Centric_Approach_for_Efficient_ICCVW_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23W-2f4f4f)]() [![Star](https://img.shields.io/github/stars/Maelic/VG_curated.svg?style=social&label=Star)](https://github.com/Maelic/VG_curated)

+ [**Vision Relation Transformer for Unbiased Scene Graph Generation**](https://arxiv.org/pdf/2308.09472) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]() [![Star](https://img.shields.io/github/stars/visinf/veto.svg?style=social&label=Star)](https://github.com/visinf/veto)

+ [**Compositional Feature Augmentation for Unbiased Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2023/papers/Li_Compositional_Feature_Augmentation_for_Unbiased_Scene_Graph_Generation_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]() [![Star](https://img.shields.io/github/stars/HKUST-LongGroup/CFA.svg?style=social&label=Star)](https://github.com/HKUST-LongGroup/CFA)


+ [**SGTR: End-to-end Scene Graph Generation with Transformer**](https://arxiv.org/pdf/2112.12970) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Paper](https://img.shields.io/badge/TPAMI24-ffa07a)]() [![Star](https://img.shields.io/github/stars/Scarecrow0/SGTR.svg?style=social&label=Star)](https://github.com/Scarecrow0/SGTR)


+ [**The Devil Is in the Labels: Noisy Label Correction for Robust Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2022/papers/Li_The_Devil_Is_in_the_Labels_Noisy_Label_Correction_for_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Star](https://img.shields.io/github/stars/muktilin/NICE.svg?style=social&label=Star)](https://github.com/muktilin/NICE)

+ [**Unsupervised Vision-Language Parsing: Seamlessly Bridging Visual Scene Graphs with Language Structures via Dependency Relationships**](https://openaccess.thecvf.com/content/CVPR2022/papers/Lou_Unsupervised_Vision-Language_Parsing_Seamlessly_Bridging_Visual_Scene_Graphs_With_Language_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() [![Star](https://img.shields.io/github/stars/LouChao98/VLGAE.svg?style=social&label=Star)](https://github.com/LouChao98/VLGAE)


+ [**Not All Relations are Equal: Mining Informative Labels for Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2022/papers/Goel_Not_All_Relations_Are_Equal_Mining_Informative_Labels_for_Scene_CVPR_2022_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR22-8A2BE2)]() 

+ [**Fine-Grained Scene Graph Generation with Data Transfer**](https://arxiv.org/pdf/2203.11654) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]() [![Star](https://img.shields.io/github/stars/waxnkw/IETrans-SGG.pytorch.svg?style=social&label=Star)](https://github.com/waxnkw/IETrans-SGG.pytorch)


+ [**Towards Open-vocabulary Scene Graph Generation with Prompt-based Finetuning**](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136880055.pdf) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]() [![Star](https://img.shields.io/github/stars/waxnkw/IETrans-SGG.pytorch.svg?style=social&label=Star)](https://github.com/waxnkw/IETrans-SGG.pytorch)

+ [**Iterative Scene Graph Generation**](https://proceedings.neurips.cc/paper_files/paper/2022/file/99831104028c3b7e6079fd8bdcc42c8f-Paper-Conference.pdf) [![Paper](https://img.shields.io/badge/NIPS22-CD5C5C2)]() [![Star](https://img.shields.io/github/stars/ubc-vision/IterativeSG.svg?style=social&label=Star)](https://github.com/ubc-vision/IterativeSG)

+ [**Towards Open-Set Scene Graph Generation With Unknown Objects**](https://ieeexplore.ieee.org/document/9690166) [![Star](https://img.shields.io/github/stars/KanghoonYoon/hetsgg-torch.svg?style=social&label=Star)](https://github.com/MotoharuSonogashira/open-set-scene-graph-generation)

+ [**Unbiased Heterogeneous Scene Graph Generation with Relation-Aware Message Passing Neural Network**](https://ojs.aaai.org/index.php/AAAI/article/view/25435/25207) [![Paper](https://img.shields.io/badge/AAAI22-c71585)]() [![Star](https://img.shields.io/github/stars/KanghoonYoon/hetsgg-torch.svg?style=social&label=Star)](https://github.com/KanghoonYoon/hetsgg-torch)


+ [**VARSCENE: A Deep Generative Model for Realistic Scene Graph Synthesis**](https://proceedings.mlr.press/v162/verma22b/verma22b.pdf) [![Paper](https://img.shields.io/badge/ICML22-FF7F50)]()


+ [**Linguistic Structures as Weak Supervision for Visual Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2021/papers/Ye_Linguistic_Structures_As_Weak_Supervision_for_Visual_Scene_Graph_Generation_CVPR_2021_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR21-8A2BE2)]() [![Star](https://img.shields.io/github/stars/yekeren/WSSGG.svg?style=social&label=Star)](https://github.com/yekeren/WSSGG)


+ [**CogTree: Cognition Tree Loss for Unbiased Scene Graph Generation**](https://www.ijcai.org/proceedings/2021/0176.pdf) [![Paper](https://img.shields.io/badge/IJCAI21-228b22)]() [![Star](https://img.shields.io/github/stars/CYVincent/Scene-Graph-Transformer-CogTree.svg?style=social&label=Star)](https://github.com/CYVincent/Scene-Graph-Transformer-CogTree)


+ [**Unconditional Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Garg_Unconditional_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]()

+ [**Learning to Generate Scene Graph from Natural Language Supervision**](https://openaccess.thecvf.com/content/ICCV2021/papers/Zhong_Learning_To_Generate_Scene_Graph_From_Natural_Language_Supervision_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]()

+ [**Context-Aware Scene Graph Generation With Seq2Seq Transformers**](https://openaccess.thecvf.com/content/ICCV2021/papers/Lu_Context-Aware_Scene_Graph_Generation_With_Seq2Seq_Transformers_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Star](https://img.shields.io/github/stars/layer6ai-labs/SGG-Seq2Seq.svg?style=social&label=Star)](https://github.com/layer6ai-labs/SGG-Seq2Seq)

+ [**Generative Compositional Augmentations for Scene Graph Prediction**](https://openaccess.thecvf.com/content/ICCV2021/papers/Knyazev_Generative_Compositional_Augmentations_for_Scene_Graph_Prediction_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]()

+ [**Visual Distant Supervision for Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Yao_Visual_Distant_Supervision_for_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Star](https://img.shields.io/github/stars/thunlp/VisualDS.svg?style=social&label=Star)](https://github.com/thunlp/VisualDS)


+[**Sketching Image Gist: Human-Mimetic Hierarchical Scene Graph Generation**](https://arxiv.org/pdf/2007.08760)
[![Paper](https://img.shields.io/badge/ECCV20-1e90ff)]() [![Star](https://img.shields.io/github/stars/Kenneth-Wong/het-eccv20.svg?style=social&label=Star)](https://github.com/Kenneth-Wong/het-eccv20)


+ [**GPS-Net: Graph Property Sensing Network for Scene Graph Generation**](https://arxiv.org/pdf/2003.12962) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/siml3/GPS-Net.svg?style=social&label=Star)](https://github.com/siml3/GPS-Net)

+ [**Weakly Supervised Visual Semantic Parsing**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Zareian_Weakly_Supervised_Visual_Semantic_Parsing_CVPR_2020_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/alirezazareian/vspnet.svg?style=social&label=Star)](https://github.com/alirezazareian/vspnet)


+ [**Unbiased Scene Graph Generation from Biased Training**](https://arxiv.org/pdf/2003.12962) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/KaihuaTang/Scene-Graph-Benchmark.pytorch.svg?style=social&label=Star)](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch)

+ [**Graphical Contrastive Losses for Scene Graph Parsing**](https://openaccess.thecvf.com/content_CVPR_2019/papers/Zhang_Graphical_Contrastive_Losses_for_Scene_Graph_Parsing_CVPR_2019_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR19-8A2BE2)]() [![Star](https://img.shields.io/github/stars/NVIDIA/ContrastiveLosses4VRD.svg?style=social&label=Star)](https://github.com/NVIDIA/ContrastiveLosses4VRD)

+ [**Visual Relationship Detection with Language Priors**](https://arxiv.org/pdf/1608.00187) [![Paper](https://img.shields.io/badge/AAAI20-191970)]() 


+ [**Learning to Compose Dynamic Tree Structures for Visual Contexts**](https://openaccess.thecvf.com/content_CVPR_2019/papers/Tang_Learning_to_Compose_Dynamic_Tree_Structures_for_Visual_Contexts_CVPR_2019_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR19-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/KaihuaTang/VCTree-Scene-Graph-Generation.svg?style=social&label=Star)](https://github.com/KaihuaTang/VCTree-Scene-Graph-Generation)

+ [**Knowledge-Embedded Routing Network for Scene Graph Generation**](https://openaccess.thecvf.com/content_CVPR_2019/papers/Chen_Knowledge-Embedded_Routing_Network_for_Scene_Graph_Generation_CVPR_2019_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR19-8A2BE2)]() 

+ [**Scene Graph Prediction with Limited Lab**](https://openaccess.thecvf.com/content_ICCV_2019/papers/Chen_Scene_Graph_Prediction_With_Limited_Labels_ICCV_2019_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV19-2f4f4f)]() 

+ [**Neural motifs: Scene graph parsing with global context**](https://openaccess.thecvf.com/content_cvpr_2018/papers/Zellers_Neural_Motifs_Scene_CVPR_2018_paper.pdf)  [![Paper](https://img.shields.io/badge/CVPR18-8A2BE2)]() [![Star](https://img.shields.io/github/stars/rowanz/neural-motifs.svg?style=social&label=Star)](https://github.com/rowanz/neural-motifs)

+ [**Scene Graph Generation From Objects, Phrases and Region Captions**](https://openaccess.thecvf.com/content_ICCV_2017/papers/Li_Scene_Graph_Generation_ICCV_2017_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV17-2f4f4f)]() [![Star](https://img.shields.io/github/stars/yikang-li/MSDN.svg?style=social&label=Star)](https://github.com/yikang-li/MSDN)


+ [**Visual Relationship Detection with Language Priors**](https://arxiv.org/pdf/1608.00187) [![Paper](https://openaccess.thecvf.com/content_cvpr_2017/papers/Xu_Scene_Graph_Generation_CVPR_2017_paper.pdf)]()   [![Paper](https://img.shields.io/badge/CVPR17-8A2BE2)]()







## Panoptic Scene Graph Generation

Compared with traditional scene graph, each object is grounded by `a panoptic segmentation mask` in PSG, achieving a compresensive structured scene representation.

+ [**SPADE: Spatial-Aware Denoising Network for Open-vocabulary Panoptic Scene Graph Generation with Long- and Local-range Context Reasoning**](https://arxiv.org/pdf/2507.05798) [![Paper](https://img.shields.io/badge/ICCV25-00CED1)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://8078qwe.github.io/SPADE/)
<details><summary>a novel spatialaware diffusion-based framework for open-vocabulary
PSG</summary>In this paper, they introduced SPADE, a novel spatialaware diffusion-based framework for open-vocabulary PSG. SPADE addresses the limitations of VLM-based PSG models, particularly their weaknesses in spatial relation reasoning. Our approach consists of two key steps: inversion-guided calibration and spatial-aware context reasoning. First, we fine-tune a pre-trained teacher diffusion model into a PSG-specific denoising network using crossattention maps from inversion, optimized with a lightweight LoRA-based calibration strategy. Second, we introduce a spatial-aware relation graph transformer that captures both local and long-range contextual dependencies, improving relation query generation</details>


+ [**Relation-R1: Cognitive Chain-of-Thought Guided Reinforcement Learning for Unified Relational Comprehension**](https://arxiv.org/pdf/2504.14642) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()  [![Star](https://img.shields.io/github/stars/HKUST-LongGroup/Relation-R1.svg?style=social&label=Star)](https://github.com/HKUST-LongGroup/Relation-R1)
  <details><summary>R1-enhanced Visual Relation Reasoning</summary>This work introduces a R1-based Unified framework for joint binary and N-ary relation reasoning with grounded cues.</details>


+ [**Pair then Relation: Pair-Net for Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2307.08699) [![Paper](https://img.shields.io/badge/TPAMI-ffa07a)]() [![Star](https://img.shields.io/github/stars/king159/Pair-Net.svg?style=social&label=Star)](https://github.com/king159/Pair-Net)



+ [**From Easy to Hard: Learning Curricular Shape-aware Features for Robust Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2407.09191)  [![Paper](https://img.shields.io/badge/IJCV24-b22222)]()


+ [**A Fair Ranking and New Model for Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2407.09216) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/lorjul/fair-psgg.svg?style=social&label=Star)](https://github.com/lorjul/fair-psgg)

+ [**OpenPSG: Open-set Panoptic Scene Graph Generation via Large Multimodal Models**](https://arxiv.org/pdf/2407.11213) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/franciszzj/OpenPSG.svg?style=social&label=Star)](https://github.com/franciszzj/OpenPSG)

+ [**Panoptic scene graph generation with semantics-prototype learning**](https://ojs.aaai.org/index.php/AAAI/article/view/28098)[![Paper](https://img.shields.io/badge/AAAI24-c71585)]() [![Star](https://img.shields.io/github/stars/lili0415/PSG-biased-annotation.svg?style=social&label=Star)](https://github.com/lili0415/PSG-biased-annotation)

+ [**TextPSG: Panoptic Scene Graph Generation from Textual Descriptions**](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhao_TextPSG_Panoptic_Scene_Graph_Generation_from_Textual_Descriptions_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]() [![Star](https://img.shields.io/github/stars/chengyzhao/TextPSG.svg?style=social&label=Star)](https://github.com/chengyzhao/TextPSG)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://vis-www.cs.umass.edu/TextPSG/)

+ [**HiLo: Exploiting high low frequency relations for unbiased panoptic scene graph generation**](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhou_HiLo_Exploiting_High_Low_Frequency_Relations_for_Unbiased_Panoptic_Scene_ICCV_2023_paper.pdf)  [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]() [![Star](https://img.shields.io/github/stars/franciszzj/HiLo.svg?style=social&label=Star)](https://github.com/franciszzj/HiLo)

+ [**Haystack: A Panoptic Scene Graph Dataset to Evaluate Rare Predicate Classes**](https://openaccess.thecvf.com/content/ICCV2023W/SG2RL/papers/Lorenz_Haystack_A_Panoptic_Scene_Graph_Dataset_to_Evaluate_Rare_Predicate_ICCVW_2023_paper.pdf)  [![Paper](https://img.shields.io/badge/ICCV23-00CED1)]() [![Star](https://img.shields.io/github/stars/lorjul/haystack.svg?style=social&label=Star)](https://github.com/lorjul/haystack) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://lorjul.github.io/haystack/)

+ [**Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2207.11247) [![Paper](https://img.shields.io/badge/ECCV22-1e90ff)]() [![Star](https://img.shields.io/github/stars/Jingkang50/OpenPSG.svg?style=social&label=Star)](https://github.com/Jingkang50/OpenPSG)


+ [**Segmentation-grounded Scene Graph Generation**](https://openaccess.thecvf.com/content/ICCV2021/papers/Khandelwal_Segmentation-Grounded_Scene_Graph_Generation_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-00CED1)]() [![Star](https://img.shields.io/github/stars/ubc-vision/segmentation-sg.svg?style=social&label=Star)](https://github.com/ubc-vision/segmentation-sg) 


+ [**Deep Generative Probabilistic Graph Neural Networks for Scene Graph Generation**](https://ojs.aaai.org/index.php/AAAI/article/view/6783) [![Paper](https://img.shields.io/badge/AAAI20-c71585)]() [![Star](https://img.shields.io/github/stars/ubc-vision/segmentation-sg.svg?style=social&label=Star)](https://github.com/ubc-vision/segmentation-sg) 










## Spatio-Temporal (Video) Scene Graph Generation

Spatio-Temporal (Video) Scene Graph Generation, a.k.a, dynamic scene graph generation, aims to provide a detailed and structured interpretation of the whole scene by parsing an event into a sequence of interactions between different visual entities. It ususally involves two subtasks:

- `Scene graph detection`: aims to generate scene graphs for given videos, comprising detection results of subject-object pari and the associatde predicates. The localization of object prediction is considered accurate when the Intersection over Union (IoU) between the prediction and ground truth is greater than 0.5.
- `Predicate classification`: classifiy predicates for given oracle detection results of subject-object pairs.
- <details><summary>Noted</summary>Noted: Evaluation is conducted with two settings: ***With Constraint*** and ***No constraints***. In the former the generated graphs are restricted to at most one edge, i.e., each subject-object pair is allowed only one predicate and in the latter, the graphs can have multiple edges. More details can refer to <a href="https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch/blob/master/METRICS.md">Metrics</a>.</details>


### LLM-based 


+ [**What can Off-the-Shelves Large Multi-Modal Models do for Dynamic Scene Graph Generation?**](https://arxiv.org/pdf/2503.15846) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 


+ [**Weakly Supervised Video Scene Graph Generation via Natural Language Supervision**](https://arxiv.org/pdf/2502.15370) [![Paper](https://img.shields.io/badge/ICLR25-696969)]()   [![Star](https://img.shields.io/github/stars/rlqja1107/NL-VSGG.svg?style=social&label=Star)](https://github.com/rlqja1107/NL-VSGG)

+ [**Tri-modal Confluence with Temporal Dynamics for Scene Graph Generation in Operating Rooms**](https://arxiv.org/pdf/2404.09231) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()






### Non-LLM-based

+ [**FROSS: Faster-than-Real-Time Online 3D Semantic Scene Graph Generation from RGB-D Images**](https://projects.howardkhh.net/FROSS/) [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)](https://openaccess.thecvf.com/content/ICCV2025/html/Hou_FROSS_Faster-Than-Real-Time_Online_3D_Semantic_Scene_Graph_Generation_from_RGB-D_ICCV_2025_paper.html) [![Star](https://img.shields.io/github/stars/XZPKU/TRKT.svg?style=social&label=Star)](https://github.com/Howardkhh/FROSS)

+ [**End-to-End Entity-Predicate Association Reasoning for Dynamic Scene Graph Generation**](https://iccv.thecvf.com/virtual/2025/poster/164)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]() 


+ [**TRKT:Weakly Supervised Dynamic Scene Graph Generation with Temporal-enhanced Relation-aware Knowledge Transferring**](https://arxiv.org/pdf/2508.04943) [![Paper](https://img.shields.io/badge/ICCV25-00CED1)]() [![Star](https://img.shields.io/github/stars/XZPKU/TRKT.svg?style=social&label=Star)](https://github.com/XZPKU/TRKT)

+ [**DIFFVSGG: Diffusion-Driven Online Video Scene Graph Generation**](https://arxiv.org/pdf/2503.13957v1) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() [![Star](https://img.shields.io/github/stars/kagawa588/DiffVsgg.svg?style=social&label=Star)](https://github.com/kagawa588/DiffVsgg)

+ [**Towards Unbiased and Robust Spatio-Temporal Scene Graph Generation and Anticipation**](https://arxiv.org/pdf/2411.13059) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/rohithpeddi/ImparTail.svg?style=social&label=Star)](https://github.com/rohithpeddi/ImparTail)

+ [**HyperGLM: HyperGraph for Video Scene Graph Generation and Anticipation**](https://openaccess.thecvf.com/content/CVPR2025/papers/Nguyen_HyperGLM_HyperGraph_for_Video_Scene_Graph_Generation_and_Anticipation_CVPR_2025_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()

+ [**SAMJAM: Zero-Shot Video Scene Graph Generation for Egocentric Kitchen Videos**](https://arxiv.org/pdf/2504.07867) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Salient Temporal Encoding for Dynamic Scene Graph Generation**](https://arxiv.org/pdf/2503.14524) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()  

+ [**SAMJAM: Zero-Shot Video Scene Graph Generation for Egocentric Kitchen Videos**](https://arxiv.org/pdf/2504.07867) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 
 
+ [**Motion-aware Contrastive Learning for Temporal Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2412.07160) [![Paper](https://img.shields.io/badge/AAAI25-c71585)]()

+ [**Towards Scene Graph Anticipation**](https://arxiv.org/pdf/2403.04899v1) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/rohithpeddi/SceneSayer.svg?style=social&label=Star)](https://github.com/rohithpeddi/SceneSayer)


+ [**End-to-end Open-vocabulary Video Visual Relationship Detection using Multi-modal Prompting**](https://arxiv.org/pdf/2409.12499) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**CYCLO: Cyclic Graph Transformer Approach to Multi-Object Relationship Modeling in Aerial Videos**](https://arxiv.org/pdf/2406.01029) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**OED: Towards One-stage End-to-End Dynamic Scene Graph Generation**](https://arxiv.org/pdf/2405.16925) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/guanw-pku/OED.svg?style=social&label=Star)](https://github.com/guanw-pku/OED) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/oed-cvpr24/%E9%A6%96%E9%A1%B5)

+ [**Action Scene Graphs for Long-Form Understanding of Egocentric Videos**](https://openaccess.thecvf.com/content/CVPR2024/papers/Rodin_Action_Scene_Graphs_for_Long-Form_Understanding_of_Egocentric_Videos_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/fpv-iplab/EASG.svg?style=social&label=Star)](https://github.com/fpv-iplab/EASG)


+ [**HIG: Hierarchical Interlacement Graph Approach to Scene Graph Generation in Video Understanding**](https://arxiv.org/pdf/2312.03050) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://uark-cviu.github.io/ASPIRe/) <details><summary>Summary</summary>Introduce a new dataset which delves into interactivities understanding within visual content by deriving scene graph representations from dense interactivities among humans and objects</details>

+ [**Action Scene Graphs for Long-Form Understanding of Egocentric Videos**](https://arxiv.org/pdf/2312.03391) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/fpv-iplab/EASG.svg?style=social&label=Star)](https://github.com/fpv-iplab/EASG)


+ [**End-to-End Video Scene Graph Generation With Temporal Propagation Transformer**](https://ieeexplore.ieee.org/document/10145598) [![Paper](https://img.shields.io/badge/TMM23-556b2f)]()


+ [**Unbiased scene graph generation in videos**](https://openaccess.thecvf.com/content/CVPR2023/papers/Nag_Unbiased_Scene_Graph_Generation_in_Videos_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/sayaknag/unbiasedSGG.svg?style=social&label=Star)](https://github.com/sayaknag/unbiasedSGG)

+ [**Panoptic Video Scene Graph Generation**](https://openaccess.thecvf.com/content/CVPR2023/papers/Yang_Panoptic_Video_Scene_Graph_Generation_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/LilyDaytoy/OpenPVSG.svg?style=social&label=Star)](https://github.com/LilyDaytoy/OpenPVSG)

+ [**Cross-Modality Time-Variant Relation Learning for Generating Dynamic Scene Graphs**](https://arxiv.org/abs/2305.08522) [![Paper](https://img.shields.io/badge/ICRA23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/qncsn2016/TR2.svg?style=social&label=Star)](https://github.com/qncsn2016/TR2)

+ [**Video Scene Graph Generation from Single-Frame Weak Supervision**](https://openreview.net/pdf?id=KLrGlNoxzb4) [![Paper](https://img.shields.io/badge/ICLR23-696969)]() [![Star](https://img.shields.io/github/stars/zjucsq/PLA.svg?style=social&label=Star)](https://github.com/zjucsq/PLA)

+ [**Prior Knowledge-driven Dynamic Scene Graph Generation with Causal Inference**](https://dl.acm.org/doi/10.1145/3581783.3612249)  [![Paper](https://img.shields.io/badge/MM23-8b4513)]()

+ [**Exploiting Long-Term Dependencies for Generating Dynamic Scene Graphs**](https://arxiv.org/pdf/2112.09828) [![Paper](https://img.shields.io/badge/ICLR23-696969)]() [![Star](https://img.shields.io/github/stars/Shengyu-Feng/DSG-DETR.svg?style=social&label=Star)](https://github.com/Shengyu-Feng/DSG-DETR)

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
Given a 3D point cloud $P \in R^{N×3}$ consisting of $N$ points, we assume there is a set of class-agnostic instance masks $M = \{M_1, ..., M_K\}$ corresponding to $K$ entities in $P$, `3D Scene Graph Generation` aims to map the input 3D point cloud to a reliable semantically structured scene graph $G = \{O, R\}$. 
Compared with 2D scene graph Generation, the input of 3D SGG is point cloud.


+ [**Statistical Confidence Rescoring for Robust 3D Scene Graph Generation from Multi-View Images**](https://arxiv.org/pdf/2508.06546)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://qixun1.github.io/projects/SCRSSG/)


+ [**Open-Vocabulary Functional 3D Scene Graphs for Real-World Indoor Spaces**](https://arxiv.org/pdf/2503.19199)  [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://openfungraph.github.io/)




+ **Blief Scene Graph**

  A utility-enhanced extension of a given incomplete scene graph $G^{'}$, by incorporating objects in $C$ (i.e., the object sets relevant for a robotic mission) into $G^{'}$, using the learnt CECI (i.e., Computation of Expectation of finding objects in $C$ based on Correlation Information) information. Belief Scene Graphs enable highlevel reasoning and optimized task planning involving set $C$, which was impossible with the incomplete $G^{'}$.
  <details><summary>中文解释</summary>“信念场景图” (Belief Scene Graphs, BSG), 它是对传统3D场景图的扩展，旨在利用局部信息进行高效的高级任务规划。论文的核心在于提出了一种基于图的学习方法，用于计算3D场景图上的“信念”（belief），也称为“期望”（expectation）。这种期望被用来策略性地添加新的节点（称为“盲节点”blind nodes），这些节点与机器人任务相关，但尚未被实际观察到。</details>

  + [**Estimating Commonsense Scene Composition on Belief Scene Graphs**](https://arxiv.org/pdf/2505.02405) [![Paper](https://img.shields.io/badge/ICRA2025-b22222)]()

  + [**Belief Scene Graphs: Expanding Partial Scenes with Object through Computation of Expectation**](https://arxiv.org/pdf/2402.03840) [![Paper](https://img.shields.io/badge/ICRA2024-b22222)]()



+ [**GaussianGraph: 3D Gaussian-based Scene Graph Generation for Open-world Scene Understanding**](https://arxiv.org/pdf/2503.04034) [![Paper](https://img.shields.io/badge/IROS2025-b22222)]() [![Star](https://img.shields.io/github/stars/WangXihan-bit/GaussianGraph.svg?style=social&label=Star)](https://github.com/WangXihan-bit/GaussianGraph)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://wangxihan-bit.github.io/GaussianGraph/)

+ [**DynamicGSG: Dynamic 3D Gaussian Scene Graphs for Environment Adaptation**](https://arxiv.org/pdf/2502.15309) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Star](https://img.shields.io/github/stars/GeLuzhou/Dynamic-GSG.svg?style=social&label=Star)](https://github.com/GeLuzhou/Dynamic-GSG)

+ [**ConceptGraphs: Open-Vocabulary 3D Scene Graphs for Perception and Planning**](https://arxiv.org/pdf/2309.16650) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/concept-graphs/concept-graphs.svg?style=social&label=Star)](https://github.com/concept-graphs/concept-graphs)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://concept-graphs.github.io/)

+ [**Point2Graph: An End-to-end Point Cloud-based 3D Open-Vocabulary Scene Graph for Robot Navigation**](https://arxiv.org/pdf/2409.10350) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://point2graph.github.io/)

+ [**Heterogeneous Graph Learning for Scene Graph Prediction in 3D Point Clouds**](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/03785.pdf) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]()

+ [**EchoScene: Indoor Scene Generation via Information Echo over Scene Graph Diffusion**](https://arxiv.org/pdf/2405.00915) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/ymxlzgy/echoscene.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/echoscene)

+ [**Weakly-Supervised 3D Scene Graph Generation via Visual-Linguistic Assisted Pseudo-labeling**](https://arxiv.org/pdf/2404.02527) [![Paper](https://img.shields.io/badge/arXiv24-b22222)](https://arxiv.org/pdf/2309.15702)  

+ [**SGRec3D: Self-Supervised 3D Scene Graph Learning via Object-Level Scene Reconstruction**](https://arxiv.org/pdf/2309.15702)  [![Paper](https://img.shields.io/badge/WACV24-800080)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://kochsebastian.com/sgrec3d)

+ [**Open3DSG: Open-Vocabulary 3D Scene Graphs from Point Clouds with Queryable Objects and Open-Set Relationships**](https://kochsebastian.com/open3dsg) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/boschresearch/Open3DSG.svg?style=social&label=Star)](https://github.com/boschresearch/Open3DSG) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://kochsebastian.com/open3dsg)

+ [**CLIP-Driven Open-Vocabulary 3D Scene Graph Generation via Cross-Modality Contrastive Learning**](https://openaccess.thecvf.com/content/CVPR2024/papers/Chen_CLIP-Driven_Open-Vocabulary_3D_Scene_Graph_Generation_via_Cross-Modality_Contrastive_Learning_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]()

+ [**Incremental 3D Semantic Scene Graph Prediction from RGB Sequences**](https://openaccess.thecvf.com/content/CVPR2023/papers/Wu_Incremental_3D_Semantic_Scene_Graph_Prediction_From_RGB_Sequences_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://shunchengwu.github.io/MonoSSG)

+ [**VL-SAT: Visual-Linguistic Semantics Assisted Training for 3D Semantic Scene Graph Prediction in Point Cloud**](https://arxiv.org/pdf/2303.14408) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]() [![Star](https://img.shields.io/github/stars/wz7in/CVPR2023-VLSAT.svg?style=social&label=Star)](https://github.com/wz7in/CVPR2023-VLSAT)

+ [**3D Spatial Multimodal Knowledge Accumulation for Scene Graph Prediction in Point Cloud**](https://openaccess.thecvf.com/content/CVPR2023/papers/Feng_3D_Spatial_Multimodal_Knowledge_Accumulation_for_Scene_Graph_Prediction_in_CVPR_2023_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR23-8A2BE2)]()

+ [**Aria Digital Twin: A New Benchmark Dataset for Egocentric 3D Machine Perception**](https://openaccess.thecvf.com/content/ICCV2023/papers/Pan_Aria_Digital_Twin_A_New_Benchmark_Dataset_for_Egocentric_3D_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://www.projectaria.com/datasets/adt/)

+ [**Lang3DSG: Language-based contrastive pre-training for 3D Scene Graph prediction**](https://arxiv.org/pdf/2310.16494) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://kochsebastian.com/lang3dsg)

+ [**SceneGraphFusion: Incremental 3D Scene Graph Prediction from RGB-D Sequences**](https://openaccess.thecvf.com/content/CVPR2021/papers/Wu_SceneGraphFusion_Incremental_3D_Scene_Graph_Prediction_From_RGB-D_Sequences_CVPR_2021_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR21-8A2BE2)]() [![Star](https://img.shields.io/github/stars/ShunChengWu/SceneGraphFusion.svg?style=social&label=Star)](https://github.com/ShunChengWu/SceneGraphFusion) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://shunchengwu.github.io/SceneGraphFusion)

+ [**Exploiting Edge-Oriented Reasoning for 3D Point-based Scene Graph Analysis**](https://arxiv.org/pdf/2103.05558) [![Paper](https://img.shields.io/badge/CVPR21-8A2BE2)]() [![Star](https://img.shields.io/github/stars/chaoyivision/SGGpoint.svg?style=social&label=Star)](https://github.com/chaoyivision/SGGpoint) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sggpoint.github.io/)


+ [**Learning 3D Semantic Scene Graphs from 3D Indoor Reconstructions**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wald_Learning_3D_Semantic_Scene_Graphs_From_3D_Indoor_Reconstructions_CVPR_2020_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/ShunChengWu/3DSSG.svg?style=social&label=Star)](https://github.com/ShunChengWu/3DSSG) 

+ [**3D Scene Graph: A Structure for Unified Semantics, 3D Space, and Camera**](https://openaccess.thecvf.com/content_ICCV_2019/papers/Armeni_3D_Scene_Graph_A_Structure_for_Unified_Semantics_3D_Space_ICCV_2019_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV19-2f4f4f)]() [![Star](https://img.shields.io/github/stars/StanfordVL/3DSceneGraph.svg?style=social&label=Star)](https://github.com/StanfordVL/3DSceneGraph) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://3dscenegraph.stanford.edu/)




## 4D Scene Graph Gnereation

+ [**EgoExOR: An Ego-Exo-Centric Operating Room Dataset for Surgical Activity Understanding**](https://arxiv.org/pdf/2505.24287)  ![Paper](https://img.shields.io/badge/arXiv25-b22222)  [![Star](https://img.shields.io/github/stars/ardamamur/EgoExOR.svg?style=social&label=Star)](https://github.com/ardamamur/EgoExOR) 

 + [**Learning 4D Panoptic Scene Graph Generation from Rich 2D Visual Scene**](https://arxiv.org/abs/2503.15019) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()

 + [**MM-OR: A Large Multimodal Operating Room Dataset for Semantic Understanding of High-Intensity Surgical Environments**](https://arxiv.org/pdf/2503.02579)  [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() [![Star](https://img.shields.io/github/stars/egeozsoy/MM-OR.svg?style=social&label=Star)](https://github.com/egeozsoy/MM-OR)

+ [**4D Panoptic Scene Graph Generation**](https://arxiv.org/pdf/2405.10305) [![Paper](https://img.shields.io/badge/NIPS23-CD5C5C2)]()  [![Star](https://img.shields.io/github/stars/Jingkang50/PSG4D.svg?style=social&label=Star)](https://github.com/Jingkang50/PSG4D)


+ [**RealGraph: A Multiview Dataset for 4D Real-world Context Graph Generation**](https://openaccess.thecvf.com/content/ICCV2023/papers/Lin_RealGraph_A_Multiview_Dataset_for_4D_Real-world_Context_Graph_Generation_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]()  [![Star](https://img.shields.io/github/stars/THU-luvision/RealGraph.svg?style=social&label=Star)](https://github.com/THU-luvision/RealGraph)



## Textual Scene Graph Generation

+ [**DiscoSG: Towards Discourse-Level Text Scene Graph Parsing through Iterative Graph Refinement**](https://arxiv.org/abs/2506.15583) ![Paper](https://img.shields.io/badge/arXiv25-b22222) [![Star](https://img.shields.io/github/stars/ShaoqLin/DiscoSG.svg?style=social&label=Star)](https://github.com/ShaoqLin/DiscoSG) 

+ [**LLM Meets Scene Graph: Can Large Language Models Understand and Generate Scene Graphs? A Benchmark and Empirical Study**](https://arxiv.org/pdf/2505.19510) [![Paper](https://img.shields.io/badge/ACL25-191970)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://tsg-bench.netlify.app/)


+ [**FACTUAL: A Benchmark for Faithful and Consistent Textual Scene Graph Parsing**](https://arxiv.org/pdf/2305.17497) [![Paper](https://img.shields.io/badge/ACL23-191970)]()  [![Star](https://img.shields.io/github/stars/zhuang-li/FactualSceneGraph.svg?style=social&label=Star)](https://github.com/zhuang-li/FactualSceneGraph) 

+ [**Scene Graph Parsing via Abstract Meaning Representation in Pre-trained Language Models**](https://aclanthology.org/2022.dlg4nlp-1.4.pdf) [![Paper](https://img.shields.io/badge/DLG4NLP22-deb887)]() 

+ [**Scene Graph Parsing by Attention Graph**](https://arxiv.org/pdf/1909.06273) [![Paper](https://img.shields.io/badge/NIPS18-CD5C5C2)]()

+ [**Scene Graph Parsing as Dependency Parsing**](https://www.cs.jhu.edu/~cxliu/papers/sgparser_naacl18.pdf) [![Paper](https://img.shields.io/badge/NAACL18-191970)]() [![Star](https://img.shields.io/github/stars/Yusics/bist-parser.svg?style=social&label=Star)](https://github.com/Yusics/bist-parser/tree/sgparser) 

+ [**Generating Semantically Precise Scene Graphs from Textual Descriptions for Improved Image Retrieval**](https://nlp.stanford.edu/pubs/schuster-krishna-chang-feifei-manning-vl15.pdf) [![Paper](https://img.shields.io/badge/VL15-191970)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://nlp.stanford.edu/software/scenegraph-parser.shtml)


## Map Space Scene Graph
+ [**Can Large Vision Language Models Read Maps like a Human?**](https://arxiv.org/pdf/2503.14607) ![Paper](https://img.shields.io/badge/arXiv25-b22222)  [![Star](https://img.shields.io/github/stars/taco-group/MapBench.svg?style=social&label=Star)](https://github.com/taco-group/MapBench) 
    <details><summary>Map space scene graph (MSSG) as a indexing data structure for the human readable map.</summary>In this paper, we introduce MapBench—the first dataset specifically designed for human-readable, pixel-based map-based outdoor navigation, curated from complex path finding scenarios. MapBench comprises over 1600 pixel space map path finding problems from 100 diverse maps. In MapBench, LVLMs generate language-based navigation instructions given a map image and a query with beginning and end landmarks. For each map, MapBench provides Map Space Scene Graph (MSSG) as an indexing data structure to convert between natural language and evaluate VLMgenerated results. We demonstrate that MapBench significantly challenges state-of-the-art LVLMs both zero-shot prompting and a Chain-of-Thought (CoT) augmented reasoning framework that decomposes map navigation into sequential cognitive processes.</details>


## Universal Scene Graph Generation

+ [**Universal Scene Graph Generation**](https://arxiv.org/abs/2503.15005) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sqwu.top/USG/) 
  <details><summary>A novel representation capable of fully characterizing comprehensive semantic scenes from any given combination of modality inputs. </summary>Scene graph (SG) representations can neatly and efficiently describe scene semantics, which has driven sustained intensive research in SG generation. In the real world, multiple modalities often coexist, with different types, such as images, text, video, and 3D data, expressing distinct characteristics. Unfortunately, current SG research is largely confined to single-modality scene modeling, preventing the full utilization of the complementary strengths of different modality SG representations in depicting holistic scene semantics. To this end, we introduce `Universal SG (USG)`, a novel representation capable of fully characterizing comprehensive semantic scenes from any given combination of modality inputs, encompassing modality-invariant and modality-specific scenes, as shown in Fig. 1. Further, we tailor a niche-targeting USG parser, USG-Par, which effectively addresses two key bottlenecks of cross-modal object alignment and out-of-domain challenges. We design the USG-Par with modular architecture for end-to-end USG generation, in which we devise an object associator to relieve the modality gap for cross-modal object alignment. Further, we propose a text-centric scene contrasting learning mechanism to mitigate domain imbalances by aligning multimodal objects and relations with textual SGs.</details>


---




# 🥝 Scene Graph Application




## Image Retrieval

+ [**SCENIR: Visual Semantic Clarity through Unsupervised Scene Graph Retrieval**](https://arxiv.org/pdf/2505.15867) [![Paper](https://img.shields.io/badge/ICML25-FF7F50)]()  [![Star](https://img.shields.io/github/stars/nickhaidos/scenir-icml2025.svg?style=social&label=Star)](https://github.com/nickhaidos/scenir-icml2025) 

+ [**SceneGraphLoc: Cross-Modal Coarse Visual Localization on 3D Scene Graphs**](https://arxiv.org/pdf/2404.00469)  [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]()  [![Star](https://img.shields.io/github/stars/y9miao/VLSG.svg?style=social&label=Star)](https://github.com/y9miao/VLSG)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://scenegraphloc.github.io/)<details><summary>SceneGraphLoc addresses the novel problem of localizing a query image in a database of 3D scenes represented as compact multi-modal 3D scene graphs</summary></details>
 


+ [**Composing Object Relations and Attributes for Image-Text Matching**](https://arxiv.org/pdf/2406.11820)  [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]()  [![Star](https://img.shields.io/github/stars/vkhoi/cora_cvpr24.svg?style=social&label=Star)](https://github.com/vkhoi/cora_cvpr24)  
 

+ [**Cross-modal Scene Graph Matching for Relationship-aware Image-Text Retrieval**](https://openaccess.thecvf.com/content_WACV_2020/papers/Wang_Cross-modal_Scene_Graph_Matching_for_Relationship-aware_Image-Text_Retrieval_WACV_2020_paper.pdf) [![Paper](https://img.shields.io/badge/WACV20-800080)]()


+ [**Image Retrieval using Scene Graphs**](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR15-8A2BE2)]()



## Image/Video Caption 

+ [**SC-Captioner: Improving Image Captioning with Self-Correction by Reinforcement Learning**](https://arxiv.org/pdf/2508.06125) ![Paper](https://img.shields.io/badge/ICCV25-2f4f4f) [![Star](https://img.shields.io/github/stars/LuFan31/CompreCap.svg?style=social&label=Star)](https://github.com/zl2048/SC-Captioner)

+ [**Fine-Grained Video Captioning through Scene Graph Consolidation**](https://arxiv.org/pdf/2502.16427) ![Paper](https://img.shields.io/badge/arXiv25-b22222)

+ [**The Devil is in the Distributions: Explicit Modeling of Scene Content is Key in Zero-Shot Video Captioning**](https://arxiv.org/pdf/2503.23679) ![Paper](https://img.shields.io/badge/arXiv25-b22222)

+ [**Benchmarking Large Vision-Language Models via Directed Scene Graph for Comprehensive Image Captioning**](https://arxiv.org/pdf/2412.08614) [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]() [![Star](https://img.shields.io/github/stars/LuFan31/CompreCap.svg?style=social&label=Star)](https://github.com/LuFan31/CompreCap)

+ [**Graph-Based Captioning: Enhancing Visual Descriptions by Interconnecting Region Captions**](https://arxiv.org/pdf/2407.06723) [![Paper](https://img.shields.io/badge/arXiv24-b22222)](https://arxiv.org/pdf/2407.06723) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://huggingface.co/graph-based-captions)<details><summary>Introducing new dataset GBC10M</summary>Humans describe complex scenes with compositionality, using simple text descriptions enriched with links and relationships. While vision-language research has aimed to develop models with compositional understanding capabilities, this is not reflected yet in existing datasets which, for the most part, still use plain text to describe images. In this work, we propose a new annotation strategy, graph-based captioning (GBC) that describes an image using a labelled graph structure, with nodes of various types. We demonstrate that GBC can be produced automatically, using off-the-shelf multimodal LLMs and open-vocabulary detection models, by building a new dataset, GBC10M, gathering GBC annotations for about 10M images of the CC12M dataset</details>

+ [**Image-Collection Summarization Using Scene-Graph Generation With External Knowledge**](https://ieeexplore.ieee.org/document/10416832)

+ [**An Approach to Generate a Caption for an Image Collection Using Scene Graph Generation**](https://ieeexplore.ieee.org/document/10315005)

+ [**Transforming Visual Scene Graphs to Image Captions**](https://aclanthology.org/2023.acl-long.694.pdf) [![Paper](https://img.shields.io/badge/ACL23-191970)]() [![Star](https://img.shields.io/github/stars/GaryJiajia/TSG.svg?style=social&label=Star)](https://github.com/GaryJiajia/TSG)

+ [**Cross2StrA: Unpaired Cross-lingual Image Captioning with Cross-lingual Cross-modal Structure-pivoted Alignment**](https://arxiv.org/pdf/2305.12260)  [![Paper](https://img.shields.io/badge/ACL23-191970)]()

+ [**UNISON: Unpaired Cross-Lingual Image Captioning**](https://ojs.aaai.org/index.php/AAAI/article/view/21310) [![Paper](https://img.shields.io/badge/AAAI22-191970)]() 

+ [**Comprehensive Image Captioning via Scene Graph Decomposition**](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123590205.pdf) [![Paper](https://img.shields.io/badge/ECCV20-1e90ff)]()  [![Star](https://img.shields.io/github/stars/YiwuZhong/Sub-GC.svg?style=social&label=Star)](https://github.com/YiwuZhong/Sub-GC)  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://pages.cs.wisc.edu/~yiwuzhong/Sub-GC.html)

+ [**From Show to Tell: A Survey on Deep Learning-based Image Captioning**](https://arxiv.org/pdf/2107.06912) [![Paper](https://img.shields.io/badge/arXiv21-b22222)]()

+ [**Image captioning based on scene graphs: A survey**](https://www.sciencedirect.com/science/article/abs/pii/S0957417423012009) 






## 2D Image Generation

+ [**Leveraging Panoptic Scene Graph for Evaluating Fine-Grained Text-to-Image Generation**](https://iccv.thecvf.com/virtual/2025/poster/899)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]()

+ [**Scene Graph Guided Generation: Enable Accurate Relations Generation in Text-to-Image Models via Textural Rectification**](https://iccv.thecvf.com/virtual/2025/poster/1560)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]() 

+ [**SurGrID: Controllable Surgical Simulation via Scene Graph to Image Diffusion**](https://arxiv.org/pdf/2502.07945) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 

+ [**Neuro-Symbolic Scene Graph Conditioning for Synthetic Image Dataset Generation**](https://arxiv.org/pdf/2503.17224) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 


+ [**LAION-SG: An Enhanced Large-Scale Dataset for Training Complex Image-Text Models with Structural Annotations**](https://arxiv.org/pdf/2412.08580) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/mengcye/LAION-SG.svg?style=social&label=Star)](https://github.com/mengcye/LAION-SG)

+ [**Generate Any Scene: Evaluating and Improving Text-to-Vision Generation with Scene Graph Programming**](https://arxiv.org/pdf/2412.08221) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/RAIVNLab/GenerateAnyScene.svg?style=social&label=Star)](https://github.com/RAIVNLab/GenerateAnyScene) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://generate-any-scene.github.io/)

+ [**LAION-SG: An Enhanced Large-Scale Dataset for Training Complex Image-Text Models with Structural Annotations**](https://arxiv.org/pdf/2412.08580) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()  [![Star](https://img.shields.io/github/stars/mengcye/LAION-SG.svg?style=social&label=Star)](https://github.com/mengcye/LAION-SG)

+ [**SSGEdit: Bridging LLM with Text2Image Generative Model for Scene Graph-based Image Editing**](https://arxiv.org/pdf/2410.11815) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()  [![Star](https://img.shields.io/github/stars/bestzzhang/SGEdit-code.svg?style=social&label=Star)](https://github.com/bestzzhang/SGEdit-code)

+ [**SG-Adapter: Enhancing Text-to-Image Generation with Scene Graph Guidance**](https://arxiv.org/pdf/2405.15321) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**What Makes a Scene ? Scene Graph-based Evaluation and Feedback for Controllable Generation**](https://arxiv.org/pdf/2411.15435) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Generated Contents Enrichment**](https://arxiv.org/pdf/2405.03650) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Joint Generative Modeling of Scene Graphs and Images via Diffusion Models**](https://arxiv.org/pdf/2401.01130) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Image Synthesis with Graph Conditioning: CLIP-Guided Diffusion Models for Scene Graphs**](https://arxiv.org/pdf/2401.14111) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**R3CD: Scene Graph to Image Generation with Relation-Aware Compositional Contrastive Control Diffusion**](https://ojs.aaai.org/index.php/AAAI/article/view/28155)  [![Paper](https://img.shields.io/badge/AAAI24-191970)]()


+ [**Scene Graph Disentanglement and Composition for Generalizable Complex Image Generation**](https://arxiv.org/pdf/2410.00447) [![Paper](https://img.shields.io/badge/NIPS24-CD5C5C)]()

+ [**Imagine that! abstract-to-intricate text-to-image synthesis with scene graph hallucination diffusion**](https://proceedings.neurips.cc/paper_files/paper/2023/file/fa64505ebdc94531087bc81251ce2376-Paper-Conference.pdf) [![Paper](https://img.shields.io/badge/NIPS23-CD5C5C)]()


+ [**SceneGenie: Scene Graph Guided Diffusion Models for Image Synthesis**](https://openaccess.thecvf.com/content/ICCV2023W/SG2RL/papers/Farshad_SceneGenie_Scene_Graph_Guided_Diffusion_Models_for_Image_Synthesis_ICCVW_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCVW23-2f4f4f)]()


+ [**Scene Graph to Image Synthesis via Knowledge Consensus**](https://ojs.aaai.org/index.php/AAAI/article/view/25387) [![Paper](https://img.shields.io/badge/AAAI23-2f4f4f)]()

+ [**Transformer-based Image Generation from Scene Graphs**](https://arxiv.org/pdf/2303.04634) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() 

+ [**Diffusion-Based Scene Graph to Image Generation with Masked Contrastive Pre-Trainin**](https://arxiv.org/pdf/2211.11138)  [![Paper](https://img.shields.io/badge/arXiv22-b22222)]()  [![Star](https://img.shields.io/github/stars/YangLing0818/SGDiff.svg?style=social&label=Star)](https://github.com/YangLing0818/SGDiff)

+ [**OSCAR-Net: Object-centric Scene Graph Attention for Image Attribution**](https://openaccess.thecvf.com/content/ICCV2021/papers/Nguyen_OSCAR-Net_Object-Centric_Scene_Graph_Attention_for_Image_Attribution_ICCV_2021_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Star](https://img.shields.io/github/stars/exnx/oscar.svg?style=social&label=Star)](https://github.com/exnx/oscar) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://exnx.github.io/oscar/)

+ [**Semantic Image Manipulation Using Scene Graphs**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Dhamo_Semantic_Image_Manipulation_Using_Scene_Graphs_CVPR_2020_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR20-8A2BE2)]() [![Star](https://img.shields.io/github/stars/he-dhamo/simsg.svg?style=social&label=Star)](https://github.com/he-dhamo/simsg) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://he-dhamo.github.io/SIMSG/)

+ [**Image Generation from Scene Graphs**](https://openaccess.thecvf.com/content_cvpr_2018/CameraReady/0764.pdf) [![Paper](https://img.shields.io/badge/CVPR18-8A2BE2)]() [![Star](https://img.shields.io/github/stars/google/sg2im.svg?style=social&label=Star)](https://github.com/google/sg2im)



## 2D/Video Scene Visual Reasoning

+ [**Seeing Beyond the Scene: Enhancing Vision-Language Models with Interactional Reasoning**](https://arxiv.org/pdf/2505.09118) [![Paper](https://img.shields.io/badge/MM25-8b4513)]()


+ [**A Schema-Guided Reason-while-Retrieve framework for Reasoning on Scene Graphs with Large-Language-Models (LLMs)**](https://arxiv.org/pdf/2502.03450) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 

+ [**Generative Visual Commonsense Answering and Explaining with Generative Scene Graph Constructing**](https://arxiv.org/pdf/2501.09041) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 


+ [**A Schema-Guided Reason-while-Retrieve framework for Reasoning on Scene Graphs with Large-Language-Models (LLMs)**](https://arxiv.org/pdf/2502.03450) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() 


+ [**STEP: Enhancing Video-LLMs’ Compositional Reasoning by Spatio-Temporal Graph-guided Self-Training**](https://arxiv.org/pdf/2412.00161) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**SpatialRGPT: Grounded Spatial Reasoning in Vision-Language Models**](https://arxiv.org/pdf/2406.01584) [![Paper](https://img.shields.io/badge/NIPS24-CD5C5C)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://www.anjiecheng.me/SpatialRGPT) [![Star](https://img.shields.io/github/stars/AnjieCheng/SpatialRGPT.svg?style=social&label=Star)](https://github.com/AnjieCheng/SpatialRGPT) 


+ [**Towards Flexible Visual Relationship Segmentation**](https://arxiv.org/pdf/2408.08305) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() <details><summary>A single model that seamlessly integrates Visual relationship understanding has been studied separately in human-object interaction (HOI) detection, scene graph generation (SGG), and referring relationships (RR) tasks.</summary>FleVRS leverages the synergy between text and
image modalities, to ground various types of relationships from images and use
textual features from vision-language models to visual conceptual understanding.</details>


+ [**LLaVA-SG: Leveraging Scene Graphs as Visual Semantic Expression in Vision-Language Models**](https://arxiv.org/pdf/2408.16224) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


+ [**SOK-Bench: A Situated Video Reasoning Benchmark with Aligned Open-World Knowledge**](https://arxiv.org/pdf/2405.09713) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://msr3d.github.io/)


+ [**VQA-GNN: Reasoning with Multimodal Knowledge via Graph Neural Networks for Visual Question Answering**](https://openaccess.thecvf.com/content/ICCV2023/papers/Wang_VQA-GNN_Reasoning_with_Multimodal_Knowledge_via_Graph_Neural_Networks_for_ICCV_2023_paper.pdf) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]()


+ [**Graphhopper: Multi-hop Scene Graph Reasoning for Visual Question Answering**](https://arxiv.org/pdf/2107.06325) [![Paper](https://img.shields.io/badge/ISWC21-6f1977)]()



## 3D Scene Visual Reasoning

+ [**FreeQ-Graph: Free-form Querying with Semantic Consistent Scene Graph for 3D Scene Understanding**](https://arxiv.org/pdf/2506.13629) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()


+ [**GaussianGraph: 3D Gaussian-based Scene Graph Generation for Open-world Scene Understanding**](https://arxiv.org/pdf/2503.04034)  [![Paper](https://img.shields.io/badge/IROS25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://wangxihan-bit.github.io/GaussianGraph/)

+ [**SpatialRGPT: Grounded Spatial Reasoning in Vision Language Models**](https://arxiv.org/pdf/2406.01584) [![Paper](https://img.shields.io/badge/NIPS24-CD5C5C)]()  [![Star](https://img.shields.io/github/stars/AnjieCheng/SpatialRGPT.svg?style=social&label=Star)](https://github.com/AnjieCheng/SpatialRGPT) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://www.anjiecheng.me/SpatialRGPT)


+ [**SceneGPT: A Language Model for 3D Scene Understanding**](https://arxiv.org/pdf/2408.06926) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**R2G: Reasoning to Ground in 3D Scenes**](https://arxiv.org/pdf/2408.13499) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Multi-modal Situated Reasoning in 3D Scenes**](https://arxiv.org/pdf/2409.02389) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://bobbywu.com/SOKBench/) [![Star](https://img.shields.io/github/stars/MSR3D/MSR3D.svg?style=social&label=Star)](https://github.com/MSR3D/MSR3D) <details><summary>Introducing a large-scale multimodal situated reasoning dataset, scalably collected leveraging 3D scene graphs and vision-language models (VLMs) across a diverse range of real-world 3D scenes</summary>MSQA includes 251K situated question-answering pairs across 9 distinct question categories, covering complex scenarios and object modalities within 3D scenes. We introduce a novel interleaved multi-modal input setting in our benchmark to provide both texts, images, and point clouds for situation and question description, aiming to resolve ambiguity in describing situations with single-modality inputs (\eg, texts).</details>


## Anomaly Detection

+ [**Scene-Specific Anomalous Relationship Detection Using Scene Graph Summarization**](https://openaccess.thecvf.com/content/CVPR2025W/VAND/html/Lai_Scene-Specific_Anomalous_Relationship_Detection_Using_Scene_Graph_Summarization_CVPRW_2025_paper.html) [![Star](https://img.shields.io/github/stars/chancharikmitra/CCoT.svg?style=social&label=Star)](https://github.com/marow17623/SARD?tab=readme-ov-file)

## Enhanced VLM/MLLM

+ [**Semantic Compositions Enhance Vision-Language Contrastive Learning**](https://arxiv.org/pdf/2407.01408) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Compositional Chain-of-Thought Prompting for Large Multimodal Models**](https://arxiv.org/pdf/2311.17076) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/chancharikmitra/CCoT.svg?style=social&label=Star)](https://github.com/chancharikmitra/CCoT)

+ [**Dysen-VDM: Empowering Dynamics-aware Text-to-Video Diffusion with LLMs**](https://openaccess.thecvf.com/content/CVPR2024/papers/Fei_Dysen-VDM_Empowering_Dynamics-aware_Text-to-Video_Diffusion_with_LLMs_CVPR_2024_paper.pdf)  [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://haofei.vip/Dysen-VDM/)

+ [**The All-Seeing Project V2: Towards General Relation Comprehension of the Open World**](https://arxiv.org/pdf/2402.19474) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/OpenGVLab/all-seeing.svg?style=social&label=Star)](https://github.com/OpenGVLab/all-seeing) <details><summary>New dataset and New Task (Relation Conversation) </summary>we propose a novel task, termed Relation Conversation (ReC), which unifies the formulation of text generation, object localization, and relation comprehension. Based on the unified formulation, we construct the AS-V2 dataset, which consists of 127K high-quality relation conversation samples, to unlock the ReC capability for Multi-modal Large Language Models (MLLMs).</details>

+ [**The All-Seeing Project: Towards Panoptic Visual Recognition and Understanding of the Open World**](https://arxiv.org/pdf/2308.01907) [![Paper](https://img.shields.io/badge/NIPS23-CD5C5C)]() <details><summary>New dataset and a unified vision-language model for open-word panoptic visual recognition and understanding</summary>we propose a new large-scale dataset (AS-1B) for open-world panoptic visual recognition and understanding, using an economical semi-automatic data engine that combines the power of off-the-shelf vision/language models and human feedback. Moreover,  we develop a unified vision-language foundation model (ASM) for open-world panoptic visual recognition and understanding. Aligning with LLMs, our ASM supports versatile image-text retrieval and generation tasks, demonstrating impressive zero-shot capability.</details>

+ [**Cross-modal Attention Congruence Regularization for Vision-Language Relation Alignment**](https://aclanthology.org/2023.acl-long.298.pdf) [![Paper](https://img.shields.io/badge/ACL23-191970)]() 


+ [**Incorporating Structured Representations into Pretrained Vision & Language Models Using Scene Graphs**](https://aclanthology.org/2023.emnlp-main.870.pdf) [![Paper](https://img.shields.io/badge/EMNLP23-191970)]()

+ [**Fine-Grained Semantically Aligned Vision-Language Pre-Training**](https://arxiv.org/pdf/2208.02515) [![Paper](https://img.shields.io/badge/NIPS22-CD5C5C)]() [![Star](https://img.shields.io/github/stars/YYJMJC/LOUPE.svg?style=social&label=Star)](https://github.com/YYJMJC/LOUPE)

+ [**ERNIE-ViL: Knowledge Enhanced Vision-Language Representations through Scene Graphs**](https://arxiv.org/pdf/2006.16934) [![Paper](https://img.shields.io/badge/AAAI21-191970)]()  [![Star](https://img.shields.io/github/stars/zhuang-li/FactualSceneGraph.svg?style=social&label=Star)](https://github.com/zhuang-li/FactualSceneGraph) 





## Information Extraction

+ [**M3S: Scene Graph Driven Multi-Granularity Multi-Task Learning for Multi-Modal NER**](https://ieeexplore.ieee.org/abstract/document/9944151) [![Paper](https://img.shields.io/badge/TPAMI-ffa07a)]()

+ [**Information screening whilst exploiting! multimodal relation extraction with feature denoising and multimodal topic modeling**](https://arxiv.org/pdf/2305.11719) [![Paper](https://img.shields.io/badge/ACL23-191970)]()
 

+ [**Multimodal Relation Extraction with Efficient Graph Alignment**](https://njuhugn.github.io/paper/Multimodal%20Relation%20Extraction%20with%20Efficient%20Graph%20Alignment-Zheng-mm21.pdf) [![Paper](https://img.shields.io/badge/MM21-8b4513)]() [![Star](https://img.shields.io/github/stars/thecharm/Mega.svg?style=social&label=Star)](https://github.com/thecharm/Mega)



## 3D Scene Generation

+ [**Controllable 3D Outdoor Scene Generation via Scene Graphs**](https://arxiv.org/pdf/2503.07152)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]()  [![Star](https://img.shields.io/github/stars/yuhengliu02/control-3d-scene.svg?style=social&label=Star)](https://github.com/yuhengliu02/control-3d-scene)


+ [**Causal Reasoning Elicits Controllable 3D Scene Generation**](https://arxiv.org/pdf/2509.15249) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://causalstruct.github.io/) [![Star](https://img.shields.io/github/stars/gokucs/causalstruct.svg?style=social&label=Star)](https://github.com/gokucs/causalstruct)

+ [**LLM-driven Indoor Scene Layout Generation via Scaled Human-aligned Data Synthesis and Multi-Stage Preference Optimization**](https://arxiv.org/pdf/2506.07570) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Towards Terrain-Aware Task-Driven 3D Scene Graph Generation in Outdoor Environments**](https://arxiv.org/pdf/2506.06562) [![Paper](https://img.shields.io/badge/ICRA25W-b22222)]()

+ [**ScanEdit: Hierarchically-Guided Functional 3D Scan Editing**](https://arxiv.org/pdf/2504.15049)  [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://aminebdj.github.io/scanedit/)

+ [**Controllable 3D Outdoor Scene Generation via Scene Graphs**](https://arxiv.org/pdf/2503.07152) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://yuheng.ink/project-page/control-3d-scene/) [![Star](https://img.shields.io/github/stars/yuhengliu02/control-3d-scene.svg?style=social&label=Star)](https://github.com/yuhengliu02/control-3d-scene) 



+ [**MMGDreamer: Mixed-Modality Graph for Geometry-Controllable 3D Indoor Scene Generation**](https://arxiv.org/pdf/2502.05874) [![Paper](https://img.shields.io/badge/AAAI25-191970)]() [![Star](https://img.shields.io/github/stars/yangzhifeio/MMGDreamer.svg?style=social&label=Star)](https://github.com/yangzhifeio/MMGDreamer) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://yangzhifeio.github.io/project/MMGDreamer/)

+ [**Toward Scene Graph and Layout Guided Complex 3D Scene Generation**](https://arxiv.org/pdf/2412.20473) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**LAYOUTDREAMER: Physics-guided Layout for Text-to-3D Compositional Scene Generation**](https://arxiv.org/pdf/2502.01949) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**PhiP-G: Physics-Guided Text-to-3D Compositional Scene Generation**](https://arxiv.org/pdf/2502.00708) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**CAST: Component-Aligned 3D Scene Reconstruction from an RGB Image**](https://arxiv.org/pdf/2502.12894) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/cast4)

+ [**Controllable 3D Outdoor Scene Generation via Scene Graphs**](https://arxiv.org/pdf/2503.07152) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Star](https://img.shields.io/github/stars/yuhengliu02/control-3d-scene.svg?style=social&label=Star)](https://github.com/yuhengliu02/control-3d-scene) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://yuheng.ink/project-page/control-3d-scene/)

+ [**EchoScene: Indoor Scene Generation via Information Echo over Scene Graph Diffusion**](https://arxiv.org/pdf/2405.00915) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/ymxlzgy/echoscene.svg?style=social&label=Star)](https://github.com/ymxlzgy/echoscene)


+ [**INSTRUCTLAYOUT: Instruction-Driven 2D and 3D Layout Synthesis with Semantic Graph Prior**](https://arxiv.org/pdf/2407.07580) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Compositional 3D Scene Synthesis with Scene Graph Guided Layout-Shape Generation**](https://arxiv.org/pdf/2403.12848) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**Graph Canvas for Controllable 3D Scene Generation**](https://arxiv.org/pdf/2412.00091) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**GraphDreamer: Compositional 3D Scene Synthesis from Scene Graphs**](https://arxiv.org/pdf/2312.00093)  [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/GGGHSL/GraphDreamer.svg?style=social&label=Star)](https://github.com/GGGHSL/GraphDreamer) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://graphdreamer.github.io/)


+ [**CommonScenes: Generating Commonsense 3D Indoor Scenes with Scene Graph Diffusion**](https://proceedings.neurips.cc/paper_files/paper/2023/file/5fba70900a84a8fb755c48ba99420c95-Paper-Conference.pdf)   [![Paper](https://img.shields.io/badge/NIPS23-CD5C5C)]() [![Star](https://img.shields.io/github/stars/ymxlzgy/commonscenes.svg?style=social&label=Star)](https://github.com/ymxlzgy/commonscenes) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://sites.google.com/view/commonscenes)

+ [**Graph-to-3D: End-to-End Generation and Manipulation of 3D Scenes Using Scene Graphs**](https://openaccess.thecvf.com/content/ICCV2021/papers/Dhamo_Graph-to-3D_End-to-End_Generation_and_Manipulation_of_3D_Scenes_Using_Scene_ICCV_2021_paper.pdf)  [![Paper](https://img.shields.io/badge/ICCV21-2f4f4f)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://he-dhamo.github.io/Graphto3D/)



## Mitigate Hallucination 

+ [**Reefknot: A Comprehensive Benchmark for Relation Hallucination Evaluation, Analysis and Mitigation in Multimodal Large Language Models**](https://arxiv.org/pdf/2408.09429) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() <details><summary>Introducing a benchmark based on scene graph dataset</summary>Specifically, we first provide a systematic definition
of relation hallucinations, integrating perspectives from perceptive and cognitive domains.  Furthermore, we construct the relation-based corpus utilizing the representative scene graph
dataset Visual Genome (VG), from which semantic triplets follow real-world distributions</details>


+ [**BACON: Supercharge Your VLM with Bag-of-Concept Graph to Mitigate Hallucinations**](https://arxiv.org/pdf/2407.03314) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/ztyang23/BACON.svg?style=social&label=Star)](https://github.com/ztyang23/BACON) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://ztyang23.github.io/bacon-page/)

+ [**Mitigating Hallucination in Visual Language Models with Visual Supervision**](https://arxiv.org/pdf/2311.16479) [![Paper](https://img.shields.io/badge/arXiv23-b22222)]() 



## Dynamic Environment Guidance

+ [**Embodied VideoAgent: Persistent Memory from Egocentric Videos and Embodied Sensors Enables Dynamic Scene Understanding**](https://www.arxiv.org/abs/2501.00358)  [![Paper](https://img.shields.io/badge/ICCV25-2f4f4f)]()  [![Star](https://img.shields.io/github/stars/Embodied-VideoAgent/embodied-videoagent.svg?style=social&label=Star)](https://github.com/Embodied-VideoAgent/embodied-videoagent) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)]([real-stanford/semantic-abstraction](https://embodied-videoagent.github.io/))


+ [**Generating Actionable Robot Knowledge Bases by Combining 3D Scene Graphs with Robot Ontologies**](https://arxiv.org/pdf/2507.11770) [![Paper](https://img.shields.io/badge/IROS25-b22222)]()

+ [**Information-Theoretic Graph Fusion with Vision-Language-Action Model for Policy Reasoning and Dual Robotic Control**](https://www.arxiv.org/pdf/2508.05342) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Imagine, Verify, Execute: Memory-Guided Agentic Exploration with Vision-Language Models**](https://arxiv.org/pdf/2505.07815) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)]([real-stanford/semantic-abstraction](https://ive-robot.github.io/))

+ [**A Spatial Relationship Aware Dataset for Robotics**](https://arxiv.org/pdf/2506.12525) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Star](https://img.shields.io/github/stars/PengPaulWang/SpatialAwareRobotDataset.svg?style=social&label=Star)](https://github.com/PengPaulWang/SpatialAwareRobotDataset)
 
+ [**Imagine, Verify, Execute: Memory-Guided Agentic Exploration with Vision-Language Models**](https://arxiv.org/pdf/2505.07815) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)]([real-stanford/semantic-abstraction](https://ive-robot.github.io/))


+ [**Visual Environment-Interactive Planning for Embodied Complex-Question Answering**](https://arxiv.org/pdf/2504.00775) [![Paper](https://img.shields.io/badge/TCSVT25-6A8428)]()

+ [**FunGraph: Functionality Aware 3D Scene Graphs for Language-Prompted Scene Interaction**](https://arxiv.org/pdf/2503.07909) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**Domain-Conditioned Scene Graphs for State-Grounded Task Planning**](https://arxiv.org/pdf/2504.06661) [![Paper](https://img.shields.io/badge/arXiv25-b22222)]()

+ [**SG-Nav: Online 3D Scene Graph Prompting for LLM-based Zero-shot Object Navigation**](https://arxiv.org/abs/2410.08189) [![Paper](https://img.shields.io/badge/NIPS24-CD5C5C)]() [![Star](https://img.shields.io/github/stars/bagh2178/SG-Nav.svg?style=social&label=Star)](https://github.com/bagh2178/SG-Nav) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)]([real-stanford/semantic-abstraction](https://bagh2178.github.io/SG-Nav/))

+ [**Open Vocabulary 3D Scene Understanding via Geometry Guided Self-Distillation**](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/02396.pdf) [![Paper](https://img.shields.io/badge/ECCV24-1e90ff)]() [![Star](https://img.shields.io/github/stars/Wang-pengfei/GGSD.svg?style=social&label=Star)](https://github.com/Wang-pengfei/GGSD)


+ [**Semantic Abstraction: Open-World 3D Scene Understanding from 2D Vision-Language Models**](https://arxiv.org/pdf/2207.11514) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/real-stanford/semantic-abstraction.svg?style=social&label=Star)](https://github.com/real-stanford/semantic-abstraction) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://semantic-abstraction.cs.columbia.edu/)

+ [**Hierarchical Open-Vocabulary 3D Scene Graphs for Language-Grounded Robot Navigation**](https://arxiv.org/pdf/2403.17846) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/hovsg/HOV-SG.svg?style=social&label=Star)](https://github.com/hovsg/HOV-SG) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://hovsg.github.io/)


+ [**Open Scene Graphs for Open World Object-Goal Navigation**](https://arxiv.org/pdf/2407.02473) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://open-scene-graphs.github.io/)

+ [**VeriGraph: Scene Graphs for Execution Verifiable Robot Planning**](https://arxiv.org/pdf/2411.10446) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()

+ [**LLM-enhanced Scene Graph Learning for Household Rearrangement**](https://arxiv.org/pdf/2408.12093) [![Paper](https://img.shields.io/badge/SIGGRAPHASIA-24-b22222)]() <details><summary>household rearrangement</summary>The household rearrangement task involves spotting misplaced objects in
a scene and accommodate them with proper places.</details>

+ [**Situational Instructions Database: Task Guidance in Dynamic Environments**](https://arxiv.org/pdf/2406.13302) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/mindgarage/situational-instructions-database.svg?style=social&label=Star)](https://github.com/mindgarage/situational-instructions-database) <details><summary>Situational Instructions Database (SID)</summary>Situational Instructions Database (SID) is a dataset for dynamic task guidance. It contains situationally-aware instructions for performing a wide range of everyday tasks or completing scenarios in 3D environments. The dataset provides step-by-step instructions for these scenarios which are grounded in the context of the situation. This context is defined through a scenario-specific scene graph that captures the objects, their attributes, and their relations in the environment. The dataset is designed to enable research in the areas of grounded language learning, instruction following, and situated dialogue.</details>

+ [**RoboHop: Segment-based Topological Map Representation for Open-World Visual Navigation**](https://arxiv.org/pdf/2405.05792) [![Paper](https://img.shields.io/badge/ICRA24-b22222)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://oravus.github.io/RoboHop/)

+ [**LLM-Personalize: Aligning LLM Planners with Human Preferences via Reinforced Self-Training for Housekeeping Robots**]() [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/donggehan/codellmpersonalize.svg?style=social&label=Star)](https://github.com/donggehan/codellmpersonalize) [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://donggehan.github.io/projectllmpersonalize/)



## Privacy-sensitive Object Identification

+ [**Beyond Visual Appearances: Privacy-sensitive Objects Identification via Hybrid Graph Reasoning**](https://arxiv.org/pdf/2406.12736) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()


## Referring Expression Comprehension

+ [**Zero-shot Referring Expression Comprehension via Structural Similarity Between Images and Captions**](https://openaccess.thecvf.com/content/CVPR2024/papers/Han_Zero-shot_Referring_Expression_Comprehension_via_Structural_Similarity_Between_Images_and_CVPR_2024_paper.pdf) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Star](https://img.shields.io/github/stars/Show-han/Zeroshot_REC.svg?style=social&label=Star)](https://github.com/Show-han/Zeroshot_REC) <details><summary>A triplet-matching objective to fine-tune the vision-language alignment models.</summary>To mitigate this gap, we leverage large foundation models to disentangle both images and texts into triplets in the format of (subject, predicate, object). After that, grounding is accomplished by calculating the structural similarity matrix between visual and textual triplets with a VLA model, and subsequently propagate it to an instancelevel similarity matrix. Furthermore, to equip VLA models with the ability of relationship nderstanding, we design a triplet-matching objective to fine-tune the VLA models on a collection of curated dataset containing abundant entity relationships</details>



## Video Retrieval


+ [**A Review and Efficient Implementation of Scene Graph Generation Metricsl**](https://arxiv.org/pdf/2404.09616) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/lorjul/sgbench.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://lorjul.github.io/sgbench/)



## Video Generation

+ [**Dysen-VDM: Empowering Dynamics-aware Text-to-Video Diffusion with LLMs**](https://arxiv.org/pdf/2308.13812) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://haofei.vip/Dysen-VDM/)

+ [**VISAGE: Video Synthesis using Action Graphs for Surgery**](https://arxiv.org/pdf/2410.17751) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()






## Automated Driving & Intelligent Transport Systems

- Traffic scene graph is constructed thought spatial location rule. For example, using BEV rules to derive triplets like `ego-vehicle, isin, lane-3`, `ego-vehicle, to right of, pedestrian-1`, and `ego-vehicle, very near, pedestrian-2`.

+ [**T2SG: Traffic Topology Scene Graph for Topology Reasoning in Autonomous Driving**](https://openaccess.thecvf.com/content/CVPR2025/papers/Lv_T2SG_Traffic_Topology_Scene_Graph_for_Topology_Reasoning_in_Autonomous_CVPR_2025_paper.pdf)   [![Paper](https://img.shields.io/badge/CVPR25-8A2BE2)]()   [![Star](https://img.shields.io/github/stars/MICLAB-BUPT/T2SG.svg?style=social&label=Star)](https://github.com/MICLAB-BUPT/T2SG)


+ [**Collaborative Dynamic 3D Scene Graphs for Automated Driving**](https://arxiv.org/pdf/2309.06635)  [![Paper](https://img.shields.io/badge/ICRA24-b22222)]()  [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://curb.cs.uni-freiburg.de/)  [![Star](https://img.shields.io/github/stars/robot-learning-freiburg/CURB-SG.svg?style=social&label=Star)](https://github.com/robot-learning-freiburg/CURB-SG)

+ [**Hktsg: A hierarchical knowledge-guided traffic scene graph representation learning framework for intelligent vehicles**](https://ieeexplore.ieee.org/abstract/document/10491331) [![Paper](https://img.shields.io/badge/TIV24-b22222)]()


+ [**Edge Feature-Enhanced Network for Collision Risk Assessment Using Traffic Scene Graphs**](https://ieeexplore.ieee.org/abstract/document/10706588) [![Paper](https://img.shields.io/badge/TSM24-b22222)]() 


+ [**Learning from interaction-enhanced scene graph for pedestrian collision risk assessment**](https://ieeexplore.ieee.org/abstract/document/10232886) [![Paper](https://img.shields.io/badge/TIV23-b22222)]() 


+ [**Toward driving scene understanding: A paradigm and benchmark dataset for ego-centric traffic scene graph representation**](https://ieeexplore.ieee.org/abstract/document/9900075) [![Paper](https://img.shields.io/badge/JRFI22-b22222)]() 

+ [**roadscene2vec: A tool for extracting and embedding road scene-graphs**](https://www.sciencedirect.com/science/article/pii/S0950705122000739) [![Paper](https://img.shields.io/badge/KBS22-b22222)]()

+ [**Scene-Graph Augmented Data-Driven Risk Assessment of Autonomous Vehicle Decisions**](https://ieeexplore.ieee.org/abstract/document/9423525)  [![Paper](https://img.shields.io/badge/TITS22-b22222)]()
 
---


# 🤶 Evaluation Metrics

+ [**A Review and Efficient Implementation of Scene Graph Generation Metrics**](https://arxiv.org/pdf/2404.09616) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]() [![Star](https://img.shields.io/github/stars/lorjul/sgbench.svg?style=social&label=Star)]() [![Project_Page](https://img.shields.io/badge/Project_Page-00CED1)](https://lorjul.github.io/sgbench/)

+ [**Semantic Similarity Score for Measuring Visual Similarity at Semantic Level**](https://arxiv.org/pdf/2406.03865) [![Paper](https://img.shields.io/badge/arXiv24-b22222)]()



---

# 🐱‍🚀 Miscellaneous




## Workshop

+ [**2nd Workshop on Scene Graphs and Graph Representation Learning**](https://sites.google.com/view/sg2rl/index) [![Paper](https://img.shields.io/badge/CVPR24-8A2BE2)]() [![YouTube](https://badges.aleen42.com/src/youtube.svg)](https://www.youtube.com/watch?v=qvof1eiN-E0)

+ [**First ICCV Workshop on Scene Graphs and Graph Representation Learning**](https://sites.google.com/view/sg2rl/sg2rl-2023/home) [![Paper](https://img.shields.io/badge/ICCV23-2f4f4f)]() [[paper_list]](https://github.com/DmitryRyumin/ICCV-2023-Papers/blob/main/sections/2023/workshops/w-scene-graphs-and-graph-representation-learning.md)


+ [**Scene Graph Representation and Learning**](https://cs.stanford.edu/people/ranjaykrishna/sgrl/index.html) [![Paper](https://img.shields.io/badge/ICCV19-2f4f4f)]() 

+ [**DIRA Workshop and Challenge**](https://cvpr-dira.lipingyang.org/) 

+ [**Lecture 18: Scene Graphs and Graph Convolutions**](https://cs231n.stanford.edu/slides/2020/lecture_18.pdf)


## Survey
+ [**A Survey of Neurosymbolic Visual Reasoning with Scene Graphs and Common Sense Knowledge**](https://neurosymbolic-ai-journal.com/system/files/nai-paper-719.pdf)

+ [**Scene Graph Generation: A Comprehensive Survey**](https://arxiv.org/pdf/2201.00443)

+ [**A Comprehensive Survey of Scene Graphs: Generation and Application**](https://ieeexplore.ieee.org/abstract/document/9661322) [![Paper](https://img.shields.io/badge/TPAMI21-ffa07a)]()




## Insteresting Works

+ [**Group Visual Relation Detection**](https://ieeexplore.ieee.org/document/10906064)

+ [**Semantic Scene Graph for Ultrasound Image Explanation and Scanning Guidance**](https://arxiv.org/pdf/2506.19683)

+ [**Benchmarking and Improving Detail Image Caption**](https://arxiv.org/pdf/2405.19092)
  <details><summary>Utilize SG for Caption Quality Evaluation</summary>This work designs a more reliable caption evaluation metric called CAPTURE (CAPtion evaluation by exTracting and coUpling coRE information). CAPTURE extracts visual elements, e.g., objects, attributes and relations from captions, and then matches these elements through three stages, achieving the highest consistency with expert judgements over other rule-based or model-based caption metrics</details>
+ [**Visually Grounded Concept Composition**](https://arxiv.org/pdf/2109.14115)
+ [**AIMS: All-Inclusive Multi-Level Segmentation for Anything**](https://proceedings.neurips.cc/paper_files/paper/2023/file/3da292ced54290c19fc55d9dba3da793-Paper-Conference.pdf)
+ [**DMESA: Densely Matching Everything by Segmenting Anything**](https://arxiv.org/pdf/2408.00279)
+ [**PanopticRecon: Leverage Open-vocabulary Instance Segmentation for Zero-shot Panoptic Reconstruction**](https://arxiv.org/pdf/2407.01349)
+ [**R3DS: Reality-linked 3D Scenes for Panoramic Scene Understanding**](https://arxiv.org/pdf/2403.12301)
+ [**Multimodal Contextualized Semantic Parsing from Speech**](https://arxiv.org/pdf/2406.06438)

+ [**Awesome Scene Graphs**](https://github.com/huoxingmeishi/Awesome-Scene-Graphs)
+ [**awesome-scene-graph**](https://github.com/mqjyl/awesome-scene-graph)




# ⭐️ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=ChocoWu/Awesome-Scene-Graph-for-VL-Learning&type=Date)](https://star-history.com/#ChocoWu/Awesome-Scene-Graph-for-VL-Learning&Date)
