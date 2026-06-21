<div align="center">

# Awesome Dexterous Hands

[![GitHub stars](https://img.shields.io/github/stars/CyanHaze/Awesome-Dexterous-Hands?style=social)](https://github.com/CyanHaze/Awesome-Dexterous-Hands/stargazers)
[![License](https://img.shields.io/github/license/CyanHaze/Awesome-Dexterous-Hands)](./LICENSE)
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
| Embodiment transfer | Retargeting | How can this interaction become executable on a robot hand? |
| Data collection | Teleoperation | How do we collect high-quality dexterous demonstrations? |
| Contact sensing | Tactile Dexterous Hands | What does the robot hand feel during execution? |
| Execution | Dexterous Manipulation Tasks | Which task is being solved? |
| Platform | Robot Hands and Hardware | Which hand makes the behavior possible? |
| Evaluation | Datasets, Benchmarks, and Simulators | How do we compare progress? |

The intended center of gravity is **retargeting and dexterous robot-hand execution**. HOI reconstruction and tactile sensing are treated as supporting pillars, not separate unrelated lists.

---

## Categories

<ul style="list-style: none; padding: 0;">
<li style="margin-left: 0;"><a href="#surveys-and-roadmaps">Surveys and Roadmaps</a></li>
<li style="margin-left: 0;">
<details>
<summary><a href="#human-to-robot-hand-retargeting">Human-to-Robot Hand Retargeting</a></summary>
<ul>
<li><a href="#pose-level-retargeting">Pose-Level Retargeting</a></li>
<li><a href="#contact-preserving-retargeting">Contact-Preserving Retargeting</a></li>
<li><a href="#object-aware--interaction-aware-retargeting">Object-Aware / Interaction-Aware Retargeting</a></li>
<li><a href="#cross-embodiment-retargeting">Cross-Embodiment Retargeting</a></li>
<li><a href="#functional--task-aware-retargeting">Functional / Task-Aware Retargeting</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#dexterous-teleoperation-and-data-collection">Dexterous Teleoperation and Data Collection</a></summary>
<ul>
<li><a href="#glove-based-teleoperation">Glove-Based Teleoperation</a></li>
<li><a href="#vision-based-teleoperation">Vision-Based Teleoperation</a></li>
<li><a href="#mr--vr-teleoperation">MR / VR Teleoperation</a></li>
<li><a href="#portable-data-collection-systems">Portable Data Collection Systems</a></li>
<li><a href="#retargeting-free-interfaces">Retargeting-Free Interfaces</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#hoi-reconstruction-for-dexterous-manipulation">HOI Reconstruction for Dexterous Manipulation</a></summary>
<ul>
<li><a href="#hand-object-pose-reconstruction">Hand-Object Pose Reconstruction</a></li>
<li><a href="#category-agnostic-object-reconstruction">Category-Agnostic Object Reconstruction</a></li>
<li><a href="#contact-aware-hoi-reconstruction">Contact-Aware HOI Reconstruction</a></li>
<li><a href="#dynamic--articulated-hoi-reconstruction">Dynamic / Articulated HOI Reconstruction</a></li>
<li><a href="#hoi-to-robot-demonstration-conversion">HOI-to-Robot Demonstration Conversion</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#tactile-dexterous-hands">Tactile Dexterous Hands</a></summary>
<ul>
<li><a href="#tactile-sensors-for-robot-hands">Tactile Sensors for Robot Hands</a></li>
<li><a href="#fingertip-tactile-sensing">Fingertip Tactile Sensing</a></li>
<li><a href="#whole-hand--skin-tactile-sensing">Whole-Hand / Skin Tactile Sensing</a></li>
<li><a href="#slip-force-and-contact-estimation">Slip, Force, and Contact Estimation</a></li>
<li><a href="#visuo-tactile-dexterous-manipulation">Visuo-Tactile Dexterous Manipulation</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#dexterous-manipulation-tasks">Dexterous Manipulation Tasks</a></summary>
<ul>
<li><a href="#dexterous-grasping">Dexterous Grasping</a></li>
<li><a href="#in-hand-manipulation">In-Hand Manipulation</a></li>
<li><a href="#reorientation-and-rotation">Reorientation and Rotation</a></li>
<li><a href="#tool-use">Tool Use</a></li>
<li><a href="#bimanual-dexterous-manipulation">Bimanual Dexterous Manipulation</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#robot-hands-and-hardware-platforms">Robot Hands and Hardware Platforms</a></summary>
<ul>
<li><a href="#anthropomorphic-hands">Anthropomorphic Hands</a></li>
<li><a href="#low-cost--open-source-hands">Low-Cost / Open-Source Hands</a></li>
<li><a href="#hand-arm-systems">Hand-Arm Systems</a></li>
<li><a href="#end-effector-design-comparisons">End-Effector Design Comparisons</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;">
<details>
<summary><a href="#datasets-benchmarks-and-simulators">Datasets, Benchmarks, and Simulators</a></summary>
<ul>
<li><a href="#human-hand-object-datasets">Human Hand-Object Datasets</a></li>
<li><a href="#robot-dexterous-manipulation-datasets">Robot Dexterous Manipulation Datasets</a></li>
<li><a href="#tactile-datasets">Tactile Datasets</a></li>
<li><a href="#simulators-and-environments">Simulators and Environments</a></li>
<li><a href="#evaluation-protocols">Evaluation Protocols</a></li>
</ul>
</details>
</li>
<li style="margin-left: 0;"><a href="#open-source-tools-and-tutorials">Open-Source Tools and Tutorials</a></li>
<li style="margin-left: 0;"><a href="#citation">Citation</a></li>
</ul>

> **Legend**<br>
> [STAR] Recommended starting point<br>
> [CODE] Official or high-quality implementation available<br>
> [DATA] Dataset or benchmark available<br>
> **Last Updated:** 2026-06-21

---

# Dexterous Hand Resources

## Surveys and Roadmaps

- To be added.

## Human-to-Robot Hand Retargeting

This is the primary category of the repository. It covers methods that map human hand motion, hand-object demonstrations, or interaction intent to robot-hand configurations or trajectories.

### Pose-Level Retargeting

Methods that mainly align joint angles, fingertip positions, hand skeletons, or MANO-style hand poses to a robot hand.

- To be added.

### Contact-Preserving Retargeting

Methods that explicitly preserve contact points, contact topology, grasp stability, or hand-object interaction structure during retargeting.

- **TopoRetarget**, "Interaction-Preserving Retargeting for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.16272-b31b1b.svg)](https://arxiv.org/abs/2606.16272)

### Object-Aware / Interaction-Aware Retargeting

Methods that use object geometry, object pose, contact maps, penetration handling, or interaction fields rather than only hand pose.

- **DexFlow**, "A Unified Approach for Dexterous Hand Pose Retargeting and Interaction". [![arXiv](https://img.shields.io/badge/arXiv-2505.01083-b31b1b.svg)](https://arxiv.org/abs/2505.01083)

### Cross-Embodiment Retargeting

Methods that handle different robot-hand kinematics, joint limits, link geometry, actuator layouts, or action spaces.

- **UniDex**, "A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)
- **UniDexTok**, "A Unified Dexterous Hand Tokenizer from Real Data". [![arXiv](https://img.shields.io/badge/arXiv-2606.10683-b31b1b.svg)](https://arxiv.org/abs/2606.10683)

### Functional / Task-Aware Retargeting

Methods that preserve task intent, such as twisting, opening, rotating, tool use, or type-level manipulation patterns.

- **DexTwist**, "Dexterous Hand Retargeting for Twist Motion via Mixed Reality-based Teleoperation". [![arXiv](https://img.shields.io/badge/arXiv-2605.12182-b31b1b.svg)](https://arxiv.org/abs/2605.12182)
- **TypeTele**, "Releasing Dexterity in Teleoperation by Dexterous Manipulation Types". [![arXiv](https://img.shields.io/badge/arXiv-2507.01857-b31b1b.svg)](https://arxiv.org/abs/2507.01857)

## Dexterous Teleoperation and Data Collection

Teleoperation systems, interfaces, and pipelines for collecting demonstrations on dexterous robot hands.

### Glove-Based Teleoperation

- **ByteDexter Teleoperation**, "Dexterous Teleoperation of 20-DoF ByteDexter Hand via Human Motion Retargeting". [![arXiv](https://img.shields.io/badge/arXiv-2507.03227-b31b1b.svg)](https://arxiv.org/abs/2507.03227)

### Vision-Based Teleoperation

- To be added.

### MR / VR Teleoperation

- **DexTwist**, "Dexterous Hand Retargeting for Twist Motion via Mixed Reality-based Teleoperation". [![arXiv](https://img.shields.io/badge/arXiv-2605.12182-b31b1b.svg)](https://arxiv.org/abs/2605.12182)

### Portable Data Collection Systems

- **UniDex-Cap**, from "UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)

### Retargeting-Free Interfaces

- **RealDexUMI**, "A Wearable Universal Manipulation Interface for Dexterous Robot Learning". [![arXiv](https://img.shields.io/badge/arXiv-2606.06033-b31b1b.svg)](https://arxiv.org/abs/2606.06033)

## HOI Reconstruction for Dexterous Manipulation

This section covers HOI reconstruction only when it provides hand-object geometry, contact, dynamics, or demonstrations that can support dexterous manipulation.

### Hand-Object Pose Reconstruction

- **HOLD**, "Category-agnostic 3D Reconstruction of Interacting Hands and Objects from Video". [![arXiv](https://img.shields.io/badge/arXiv-2311.18448-b31b1b.svg)](https://arxiv.org/abs/2311.18448) [![GitHub](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/zc-alexfan/hold)

### Category-Agnostic Object Reconstruction

- **HandNeRF**, "Learning to Reconstruct Hand-Object Interaction Scene from a Single RGB Image". [![arXiv](https://img.shields.io/badge/arXiv-2309.07891-b31b1b.svg)](https://arxiv.org/abs/2309.07891) [![Project](https://img.shields.io/badge/Project-Page-green)](https://samsunglabs.github.io/HandNeRF-project-page/)

### Contact-Aware HOI Reconstruction

- **G-HOP**, "Generative Hand-Object Prior for Interaction Reconstruction and Grasp Synthesis". [![arXiv](https://img.shields.io/badge/arXiv-2404.12383-b31b1b.svg)](https://arxiv.org/abs/2404.12383) [![Project](https://img.shields.io/badge/Project-Page-green)](https://judyye.github.io/ghop-www)

### Dynamic / Articulated HOI Reconstruction

- **ARCTIC**, "A Dataset for Dexterous Bimanual Hand-Object Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2204.13662-b31b1b.svg)](https://arxiv.org/abs/2204.13662) [![Project](https://img.shields.io/badge/Project-Page-green)](https://arctic.is.tue.mpg.de)
- **ViTaM-D**, "Dynamic Reconstruction of Hand-Object Interaction with Distributed Force-aware Contact Representation". [![arXiv](https://img.shields.io/badge/arXiv-2411.09572-b31b1b.svg)](https://arxiv.org/abs/2411.09572)

### HOI-to-Robot Demonstration Conversion

- To be added.

## Tactile Dexterous Hands

Tactile papers are included when the sensor, representation, or policy is connected to robot hands, manipulation, contact estimation, or data collection.

### Tactile Sensors for Robot Hands

- **AnySkin**, "Plug-and-play Skin Sensing for Robotic Touch". [![arXiv](https://img.shields.io/badge/arXiv-2409.08276-b31b1b.svg)](https://arxiv.org/abs/2409.08276)

### Fingertip Tactile Sensing

- **FingerEye**, "FingerEye: In-Hand Vision-Tactile Sensor for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2604.20689-b31b1b.svg)](https://arxiv.org/abs/2604.20689)

### Whole-Hand / Skin Tactile Sensing

- **HT-Bench**, "HT-Bench: Benchmarking Full-Hand Tactile Perception for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.19161-b31b1b.svg)](https://arxiv.org/abs/2606.19161)

### Slip, Force, and Contact Estimation

- To be added.

### Visuo-Tactile Dexterous Manipulation

- **RAPID Hand**, "A Robust, Affordable, Perception-Integrated, Dexterous Manipulation Platform for Generalist Robot Autonomy". [![arXiv](https://img.shields.io/badge/arXiv-2506.07490-b31b1b.svg)](https://arxiv.org/abs/2506.07490)
- **TacSL**, "A Library for Visuotactile Sensor Simulation and Learning". [![arXiv](https://img.shields.io/badge/arXiv-2408.06506-b31b1b.svg)](https://arxiv.org/abs/2408.06506)

## Dexterous Manipulation Tasks

Task-oriented papers should be listed here even if they also appear in retargeting, tactile, or teleoperation sections.

### Dexterous Grasping

- To be added.

### In-Hand Manipulation

- To be added.

### Reorientation and Rotation

- To be added.

### Tool Use

- To be added.

### Bimanual Dexterous Manipulation

- **ARCTIC**, "A Dataset for Dexterous Bimanual Hand-Object Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2204.13662-b31b1b.svg)](https://arxiv.org/abs/2204.13662) [![Project](https://img.shields.io/badge/Project-Page-green)](https://arctic.is.tue.mpg.de)

## Robot Hands and Hardware Platforms

Robot hands, hand-arm platforms, and platform papers that include design, sensing, actuation, or reproducibility details.

### Anthropomorphic Hands

- **ByteDexter Hand**, from "Dexterous Teleoperation of 20-DoF ByteDexter Hand via Human Motion Retargeting". [![arXiv](https://img.shields.io/badge/arXiv-2507.03227-b31b1b.svg)](https://arxiv.org/abs/2507.03227)

### Low-Cost / Open-Source Hands

- **RAPID Hand**, "A Robust, Affordable, Perception-Integrated, Dexterous Manipulation Platform for Generalist Robot Autonomy". [![arXiv](https://img.shields.io/badge/arXiv-2506.07490-b31b1b.svg)](https://arxiv.org/abs/2506.07490)

### Hand-Arm Systems

- To be added.

### End-Effector Design Comparisons

- To be added.

## Datasets, Benchmarks, and Simulators

Resources for training, evaluating, or simulating dexterous hand-object manipulation.

### Human Hand-Object Datasets

- **ARCTIC**, "A Dataset for Dexterous Bimanual Hand-Object Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2204.13662-b31b1b.svg)](https://arxiv.org/abs/2204.13662) [![Project](https://img.shields.io/badge/Project-Page-green)](https://arctic.is.tue.mpg.de)

### Robot Dexterous Manipulation Datasets

- **UniDex-Dataset**, from "UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos". [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg)](https://arxiv.org/abs/2603.22264)

### Tactile Datasets

- **Sparsh / TacBench**, "Sparsh: Self-supervised Touch Representations for Vision-based Tactile Sensing". [![arXiv](https://img.shields.io/badge/arXiv-2410.24090-b31b1b.svg)](https://arxiv.org/abs/2410.24090)
- **HT-Bench**, "HT-Bench: Benchmarking Full-Hand Tactile Perception for Dexterous Manipulation". [![arXiv](https://img.shields.io/badge/arXiv-2606.19161-b31b1b.svg)](https://arxiv.org/abs/2606.19161)

### Simulators and Environments

- **TacSL**, "A Library for Visuotactile Sensor Simulation and Learning". [![arXiv](https://img.shields.io/badge/arXiv-2408.06506-b31b1b.svg)](https://arxiv.org/abs/2408.06506)

### Evaluation Protocols

- To be added.

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
