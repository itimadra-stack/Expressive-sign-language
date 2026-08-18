# Expressive Sign Language Computer Vision

This repository is a research-oriented implementation scaffold derived from the methodology and pseudocode of the study:

**Expressive Sign Language System for Deaf Kids with MPEG-4 Approach of Virtual Human Character**

## Project scope

The study describes a British Sign Language (BSL) virtual-signing system using:

- Kinect X-Box 360 for markerless motion capture
- Hand landmark / feature-point processing
- Real-world coordinate conversion from depth frames
- Feature calculation from hand-pose landmarks
- MPEG-4-based animation parameters
- Blender-based virtual character animation
- Multichannel composition involving hand motion, facial expression, lip syncing, gaze, phoneme-viseme mapping, and rendering

This repository implements the algorithmic blend logic presented in the paper and provides a clean Python scaffold for extending the method with real Kinect-derived landmark data.

## Important note

The paper provides pseudocode and methodological descriptions, but it does **not** provide a complete original software implementation, Kinect SDK integration code, or all numerical parameter values required to reproduce the full system exactly.

Therefore, this repository is a **transparent research reconstruction/scaffold** based on the paper's described algorithm, not a claim that the full original experimental software has been recovered.

## Files

- `main.py` — implementation of the blending logic and a simple hand-feature demonstration
- `requirements.txt` — minimal Python dependencies
- `METHOD.md` — mapping between the paper methodology and the code

## Run

```bash
pip install -r requirements.txt
python main.py
```

## Example output

The script creates sample hand feature points, computes pairwise distances, and applies a time-dependent blend between identity transforms and hand-point transforms.

## Future extension

To reproduce the complete experimental pipeline, real project data and implementation details would still be needed, including:

- Kinect frame acquisition
- Depth-to-world calibration constants
- Original hand landmark coordinates
- MPEG-4/FAP mapping matrix
- Blender rig / virtual character files
- Motion-capture sequences
- Facial-expression and gaze parameters

## Research areas

Computer Vision · Motion Capture · Human-Computer Interaction · Sign Language Animation · Virtual Humans · 3D Animation
