---
layout: default
---

## Abstract

Emerging applications, such as indoor navigation or facility management, present new requirements of automatic and robust partitioning of indoor 3D point clouds into rooms. Previous research is either based on the Manhattan-world assumption or relies on the availability of the scanner pose information. We address these limitations by following the architectural definition of a room, where the room is an inner free space separated from other spaces through openings or partitions. For this we formulate an anisotropic potential field for 3D environments and illustrate how it can be used for room segmentation in the proposed segmentation pipeline. The experimental results confirm that our method outperforms state-of-the-art methods on a number of datasets including those that violate the Manhattan-world assumption. 

## Basic intuition

<img src="assets/teaser.png" alt="Overview" width="500">

*Illustration of rooms as inner free spaces separated by smaller openings. Top: side view of an indoor environment with two rooms separated by a smaller room (corridor). Furniture is shown in brown, several free voxels with potential field (PF) values are also shown. Bottom: top-down view with proposed anisotropic PF maximum values along the vertical voxel stack. For voxels, red corresponds to high PF values and dark blue to low.*

## Overview of the pipeline

<img src="assets/pipeline_overview.png" alt="Overview" width="600">

*Overview of the proposed method*

## Main contributions

1. Framework to compute interior free space without assuming knowledge of scanner poses or the Manhattan-world structure of indoor environments.
2. 3D formulation of anisotropic PF computation for free space that is robust to the impact of clutter and occlusion and makes no assumptions on the room layout.

## Results

### Results for Mura et al dataset

<img src="assets/result1.png" alt="Room1" width="500">

*Results for the dataset violating the Manhattan-world assumption [3]. Top row: Modern, middle row: Cottage, bottom row: Penthouse. Left: reconstruction result of [3], middle: PF map, right: our result.*


### Results for Stanford dataset

<img src="assets/result2.png" alt="Overview" width="500">

*Fig. 4: Results for the large-scale dataset of [6]. From left to right: ground truth, results of [6], our PF map, our labeling result. Top row: Area 1, middle row: Area 2, bottom row: Area 3. Here with red ellipses we denote erroneously labeled rooms. See supplementary material for larger figures.*


### Results for Ikehata et al. dataset

<img src="assets/result3.png" alt="Overview" width="500">

*Results for the dataset of [5]. From left to right: Office 1, Office 2, Apartment 1, Apartment 2, Apartment 3. Top row: results of [5], middle row: our PF map, bottom row: our labeling result. Red ellipses denote erroneously labeled rooms. See supplementary material for larger figures.*


