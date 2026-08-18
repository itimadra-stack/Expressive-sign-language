# Method-to-Code Mapping

This document explains which parts of the study are represented in this repository.

## 1. Hand Sign Pose Computation

The study states that hand poses are represented through distances between paired landmark features computed from hand-pose coordinate points.

Implemented in:

```python
pairwise_landmark_distances(points)
```

## 2. Motion Capture

The study uses Kinect X-Box 360 as a markerless motion-capture device and discusses capturing body-joint information.

This repository does **not** fabricate Kinect acquisition code because the paper does not provide the exact SDK implementation.

## 3. Parameter Retrieval

The study describes reconstruction of finger motion, face transfer, image-frame retrieval, and conversion of Kinect frames to basic image formats.

These steps require original acquisition files / SDK details and therefore are documented as future extensions.

## 4. Feature Calculation

The study describes RGB, depth, and monochrome/depth information and says that real-world coordinates are obtained from depth-frame pixels before deriving hand-pose features.

The current code begins from already available 3D landmark coordinates.

## 5. MPEG-4 Parameter Mapping

The study refers to a parameter matrix and mapping toward MPEG-4 animation parameters.

The exact numerical mapping matrix is not supplied in the source document, so it is not invented here.

## 6. Algorithm 1 — Blender Algorithmic Blend

The paper provides pseudocode that:

1. Initializes hand feature-point weights to 1.
2. Initializes point transforms to Identity.
3. Checks whether time lies in the animation interval with fade-in/fade-out.
4. Computes a time-dependent weight.
5. Interpolates point transformations where appropriate.
6. Decreases the remaining feature-point weight.

Implemented in:

```python
algorithmic_blend(...)
blend_weight(...)
interpolate_transform(...)
```

## 7. Rendering / Blender

The paper reports using Blender for 3D character animation.

This repository currently implements the algorithmic logic only. A full Blender integration would require the original rig, character blueprint, animation data, and mapping details.
