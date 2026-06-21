<div align="center">

# Awesome Dexterous Hands

[![GitHub stars](https://img.shields.io/github/stars/CyanHaze/Awesome-Dexterous-Hands?style=social)](https://github.com/CyanHaze/Awesome-Dexterous-Hands/stargazers)
[![License](https://img.shields.io/github/license/CyanHaze/Awesome-Dexterous-Hands)](./LICENSE)
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](./CONTRIBUTING.md)

A curated list of papers, datasets, simulators, hardware platforms, and open-source resources for **dexterous robot hands**.

This repository focuses on concrete hand-object manipulation scenarios: reconstructing human hand-object interaction, retargeting or teleoperating it to robot hands, using tactile sensing for contact-rich execution, and evaluating dexterous manipulation on real tasks.

</div>

---

## News & Updates

- [2026.06] Repository scaffold launched with the first taxonomy for retargeting, HOI reconstruction, tactile dexterous hands, teleoperation, hardware, datasets, and tasks.
- [Ongoing] Paper and resource contributions are welcome. See [CONTRIBUTING.md](./CONTRIBUTING.md).

---

## Scope

This repo is **robot-hand first**. It is not a general tactile-sensing list, not a general hand-pose list, and not a general robot-manipulation list.

Included:

- Dexterous robot hands, anthropomorphic hands, multi-finger hands, and hand-arm systems.
- Human-to-robot hand retargeting, especially object-aware, contact-preserving, and cross-embodiment methods.
- Dexterous teleoperation and data collection systems.
- HOI reconstruction when it helps recover hand-object pose, contact, motion, or demonstrations for robot hands.
- Tactile sensing when it is attached to robot hands or used for dexterous manipulation.
- Datasets, simulators, benchmarks, and open-source tools for dexterous hand-object manipulation.

Excluded by default:

- Pure human hand pose estimation without object interaction.
- Pure HOI action recognition without 3D geometry, contact, or robot relevance.
- Pure tactile sensor material papers without a robot-hand or manipulation connection.
- General parallel-gripper manipulation, unless it introduces a resource directly useful for dexterous hands.
- General VLA / embodied-AI papers without a dexterous-hand component.

---

## Taxonomy Rationale

The repository is organized around a practical pipeline:

| Stage | Main section | Core question |
|---|---|---|
| Human interaction capture | HOI Reconstruction | What did the human hand and object do? |
| Embodiment transfer and data collection | Retargeting and Teleoperation | How can this interaction become executable on a robot hand? |
| Contact sensing | Tactile Dexterous Hands | What does the robot hand feel during execution? |
| Execution | Dexterous Manipulation Tasks | Which task is being solved? |
| Platform | Robot Hands and Hardware | Which hand makes the behavior possible? |
| Evaluation | Datasets, Benchmarks, and Simulators | How do we compare progress? |

The intended center of gravity is **retargeting and dexterous robot-hand execution**. HOI reconstruction and tactile sensing are treated as supporting pillars, not separate unrelated lists.

---

## Categories

<ul style="list-style: none; padding: 0;">
<li style="margin-left: 0;"><a href="#surveys-and-roadmaps">Surveys and Roadmaps</a></li>
<li style="margin-left: 0;"><a href="#retargeting-and-teleoperation">Retargeting and Teleoperation</a></li>
<li style="margin-left: 0;"><a href="#hoi-reconstruction-for-dexterous-manipulation">HOI Reconstruction for Dexterous Manipulation</a></li>
<li style="margin-left: 0;"><a href="#tactile-dexterous-hands">Tactile Dexterous Hands</a></li>
<li style="margin-left: 0;"><a href="#dexterous-manipulation-tasks">Dexterous Manipulation Tasks</a></li>
<li style="margin-left: 0;"><a href="#robot-hands-and-hardware-platforms">Robot Hands and Hardware Platforms</a></li>
<li style="margin-left: 0;"><a href="#datasets-benchmarks-and-simulators">Datasets, Benchmarks, and Simulators</a></li>
<li style="margin-left: 0;"><a href="#open-source-tools-and-tutorials">Open-Source Tools and Tutorials</a></li>
<li style="margin-left: 0;"><a href="#citation">Citation</a></li>
</ul>

> **Legend**<br>
> ⭐️ Recommended starting point<br>
> [CODE] Official or high-quality implementation available<br>
> [DATA] Dataset or benchmark available<br>
> **Last Updated:** 2026-06-21

---

# Dexterous Hand Resources

## Surveys and Roadmaps

- To be added.

## Retargeting and Teleoperation

This is the primary category of the repository. It covers methods and systems that map human hand motion, hand-object demonstrations, or interaction intent to executable robot-hand behavior.

### Retargeting Methods

- **TopoRetarget**, "Interaction-Preserving Retargeting for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.16272-b31b1b.svg)](https://arxiv.org/abs/2606.16272)
- **UniDexTok**, "A Unified Dexterous Hand Tokenizer from Real Data". [![arXiv](https://img.shields.io/badge/arXiv-2606.10683-b31b1b.svg)](https://arxiv.org/abs/2606.10683)
- **DexTwist**, "Dexterous Hand Retargeting for Twist Motion via Mixed Reality-based Teleoperation". [![arXiv](https://img.shields.io/badge/arXiv-2605.12182-b31b1b.svg)](https://arxiv.org/abs/2605.12182)
- **UniDex**, "A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)
- **TypeTele**, "Releasing Dexterity in Teleoperation by Dexterous Manipulation Types". [![arXiv](https://img.shields.io/badge/arXiv-2507.01857-b31b1b.svg)](https://arxiv.org/abs/2507.01857)
- **DexFlow**, "A Unified Approach for Dexterous Hand Pose Retargeting and Interaction". [![arXiv](https://img.shields.io/badge/arXiv-2505.01083-b31b1b.svg)](https://arxiv.org/abs/2505.01083)

### Teleoperation and Data Collection

- **RealDexUMI**, "A Wearable Universal Manipulation Interface for Dexterous Robot Learning". [![arXiv](https://img.shields.io/badge/arXiv-2606.06033-b31b1b.svg)](https://arxiv.org/abs/2606.06033)
- **UniDex-Cap**, from "UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)
- **ByteDexter Teleoperation**, "Dexterous Teleoperation of 20-DoF ByteDexter Hand via Human Motion Retargeting". [![arXiv](https://img.shields.io/badge/arXiv-2507.03227-b31b1b.svg)](https://arxiv.org/abs/2507.03227)

## HOI Reconstruction for Dexterous Manipulation

This section covers HOI reconstruction and upstream egocentric hand-motion recovery when they provide hand-object geometry, contact, dynamics, or demonstrations that can support dexterous manipulation.

### Reconstruction and Tracking

- **WHOLE**, "World-Grounded Hand-Object Lifted from Egocentric Videos". [![arXiv](https://img.shields.io/badge/arXiv-2602.22209-b31b1b.svg)](https://arxiv.org/abs/2602.22209) [![Project](https://img.shields.io/badge/Project-Page-green)](https://judyye.github.io/whole-www/)
- **AGILE**, "Hand-Object Interaction Reconstruction from Video via Agentic Generation". [![arXiv](https://img.shields.io/badge/arXiv-2602.04672-b31b1b.svg)](https://arxiv.org/abs/2602.04672)
- **EgoGrasp**, "World-Space Hand-Object Interaction Reconstruction from Egocentric Videos". [![arXiv](https://img.shields.io/badge/arXiv-2601.01050-b31b1b.svg)](https://arxiv.org/abs/2601.01050) [![Project](https://img.shields.io/badge/Project-Page-green)](https://frank-f2022.github.io/projects/EgoGrasp/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/MINT-SJTU/EgoGrasp)
- **Dyn-HaMR**, "Recovering 4D Interacting Hand Motion from a Dynamic Camera". [![Project](https://img.shields.io/badge/Project-Page-green)](https://dyn-hamr.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/ZhengdiYu/Dyn-HaMR)
- **HaWoR**, "High-fidelity Hand Motion Reconstruction in World Coordinates from Egocentric Videos". [![Project](https://img.shields.io/badge/Project-Page-green)](https://hawor-project.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/ThunderVVV/HaWoR)
- **Follow My Hold**, "Hand-Object Interaction Reconstruction through Geometric Guidance". [![arXiv](https://img.shields.io/badge/arXiv-2508.18213-b31b1b.svg)](https://arxiv.org/abs/2508.18213) [![Project](https://img.shields.io/badge/Project-Page-green)](https://aidilayce.github.io/FollowMyHold-page/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/aidilayce/FollowMyHold)
- **EmbodMoCap**, "Embodied Motion Capture: 4D Human Reconstruction in Everyday Environments". [![arXiv](https://img.shields.io/badge/arXiv-2602.23205-b31b1b.svg)](https://arxiv.org/abs/2602.23205) [![Project](https://img.shields.io/badge/Project-Page-green)](https://wenjiawang0312.github.io/projects/embodmocap/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/WenjiaWang0312/EmbodMocap)
- **ViTaM-D**, "Dynamic Reconstruction of Hand-Object Interaction with Distributed Force-aware Contact Representation". [![arXiv](https://img.shields.io/badge/arXiv-2411.09572-b31b1b.svg)](https://arxiv.org/abs/2411.09572)
- ⭐️ **WiLoR**, "End-to-End 3D Hand Localization and Reconstruction in-the-wild". [![arXiv](https://img.shields.io/badge/arXiv-2409.12259-b31b1b.svg)](https://arxiv.org/abs/2409.12259) [![Project](https://img.shields.io/badge/Project-Page-green)](https://rolpotamias.github.io/WiLoR/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/rolpotamias/WiLoR)
- **G-HOP**, "Generative Hand-Object Prior for Interaction Reconstruction and Grasp Synthesis". [![arXiv](https://img.shields.io/badge/arXiv-2404.12383-b31b1b.svg)](https://arxiv.org/abs/2404.12383) [![Project](https://img.shields.io/badge/Project-Page-green)](https://judyye.github.io/ghop-www)
- ⭐️ **HOLD**, "Category-agnostic 3D Reconstruction of Interacting Hands and Objects from Video". [![arXiv](https://img.shields.io/badge/arXiv-2311.18448-b31b1b.svg)](https://arxiv.org/abs/2311.18448) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/zc-alexfan/hold)
- **HandNeRF**, "Learning to Reconstruct Hand-Object Interaction Scene from a Single RGB Image". [![arXiv](https://img.shields.io/badge/arXiv-2309.07891-b31b1b.svg)](https://arxiv.org/abs/2309.07891) [![Project](https://img.shields.io/badge/Project-Page-green)](https://samsunglabs.github.io/HandNeRF-project-page/)

## Tactile Dexterous Hands

Tactile papers are included when the sensor, representation, or policy is connected to robot hands, manipulation, contact estimation, or data collection.

### Tactile Sensing and Perception

- **HT-Bench**, "HT-Bench: Benchmarking Full-Hand Tactile Perception for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.19161-b31b1b.svg)](https://arxiv.org/abs/2606.19161)
- **FingerEye**, "FingerEye: In-Hand Vision-Tactile Sensor for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2604.20689-b31b1b.svg)](https://arxiv.org/abs/2604.20689)
- **Sparsh / TacBench**, "Sparsh: Self-supervised Touch Representations for Vision-based Tactile Sensing". [![arXiv](https://img.shields.io/badge/arXiv-2410.24090-b31b1b.svg)](https://arxiv.org/abs/2410.24090)
- **AnySkin**, "Plug-and-play Skin Sensing for Robotic Touch". [![arXiv](https://img.shields.io/badge/arXiv-2409.08276-b31b1b.svg)](https://arxiv.org/abs/2409.08276)

### Visuo-Tactile Dexterous Manipulation

- **RAPID Hand**, "A Robust, Affordable, Perception-Integrated, Dexterous Manipulation Platform for Generalist Robot Autonomy". [![arXiv](https://img.shields.io/badge/arXiv-2506.07490-b31b1b.svg)](https://arxiv.org/abs/2506.07490)
- **TacSL**, "A Library for Visuotactile Sensor Simulation and Learning". [![arXiv](https://img.shields.io/badge/arXiv-2408.06506-b31b1b.svg)](https://arxiv.org/abs/2408.06506)

## Dexterous Manipulation Tasks

Task-oriented papers should be listed here even if they also appear in retargeting, tactile, or teleoperation sections.

- ⭐️ **ARCTIC**, "A Dataset for Dexterous Bimanual Hand-Object Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2204.13662-b31b1b.svg)](https://arxiv.org/abs/2204.13662) [![Project](https://img.shields.io/badge/Project-Page-green)](https://arctic.is.tue.mpg.de)
- To be expanded with dexterous grasping, in-hand manipulation, reorientation, tool use, and bimanual manipulation papers.

## Robot Hands and Hardware Platforms

Robot hands, hand-arm platforms, and platform papers that include design, sensing, actuation, or reproducibility details.

- **ByteDexter Hand**, from "Dexterous Teleoperation of 20-DoF ByteDexter Hand via Human Motion Retargeting". [![arXiv](https://img.shields.io/badge/arXiv-2507.03227-b31b1b.svg)](https://arxiv.org/abs/2507.03227)
- **RAPID Hand**, "A Robust, Affordable, Perception-Integrated, Dexterous Manipulation Platform for Generalist Robot Autonomy". [![arXiv](https://img.shields.io/badge/arXiv-2506.07490-b31b1b.svg)](https://arxiv.org/abs/2506.07490)
- To be expanded with anthropomorphic hands, low-cost hands, hand-arm systems, and end-effector design comparisons.

## Datasets, Benchmarks, and Simulators

Resources for training, evaluating, or simulating dexterous hand-object manipulation.

### HOI and Human Demonstration Datasets

- ⭐️ **EgoVerse**, "An Ecosystem for Curating, Accessing, and Learning from Human Data for Robot Learning". [![arXiv](https://img.shields.io/badge/arXiv-2604.07607-b31b1b.svg)](https://arxiv.org/abs/2604.07607) [![Project](https://img.shields.io/badge/Project-Page-green)](https://egoverse.ai/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/GaTech-RL2/EgoVerse)
- **UniDex-Dataset**, from "UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)
- **EmbodMoCap**, "Embodied Motion Capture: 4D Human Reconstruction in Everyday Environments". [![arXiv](https://img.shields.io/badge/arXiv-2602.23205-b31b1b.svg)](https://arxiv.org/abs/2602.23205) [![Project](https://img.shields.io/badge/Project-Page-green)](https://wenjiawang0312.github.io/projects/embodmocap/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/WenjiaWang0312/EmbodMocap)
- ⭐️ **HOT3D**, "Hand and Object Tracking in 3D from Egocentric Multi-View Videos". [![arXiv](https://img.shields.io/badge/arXiv-2411.19167-b31b1b.svg)](https://arxiv.org/abs/2411.19167) [![Project](https://img.shields.io/badge/Project-Page-green)](https://facebookresearch.github.io/hot3d/) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/facebookresearch/hot3d)
- ⭐️ **ARCTIC**, "A Dataset for Dexterous Bimanual Hand-Object Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2204.13662-b31b1b.svg)](https://arxiv.org/abs/2204.13662) [![Project](https://img.shields.io/badge/Project-Page-green)](https://arctic.is.tue.mpg.de)

### Tactile Datasets and Simulators

- **Sparsh / TacBench**, "Sparsh: Self-supervised Touch Representations for Vision-based Tactile Sensing". [![arXiv](https://img.shields.io/badge/arXiv-2410.24090-b31b1b.svg)](https://arxiv.org/abs/2410.24090)
- **HT-Bench**, "HT-Bench: Benchmarking Full-Hand Tactile Perception for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.19161-b31b1b.svg)](https://arxiv.org/abs/2606.19161)
- **TacSL**, "A Library for Visuotactile Sensor Simulation and Learning". [![arXiv](https://img.shields.io/badge/arXiv-2408.06506-b31b1b.svg)](https://arxiv.org/abs/2408.06506)

## Open-Source Tools and Tutorials

- To be added.

## Citation

If you find this repository useful, please consider citing it:

```bibtex
@misc{awesome_dexterous_hands,
  title  = {Awesome Dexterous Hands},
  author = {CyanHaze},
  year   = {2026},
  url    = {https://github.com/CyanHaze/Awesome-Dexterous-Hands}
}
```
