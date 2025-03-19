---
## 📌 A Simple Self-Supervised IMU Denoising Method for Inertial Aided Navigation
-https://github.com/KleinYuan/IMUDB
### I. Research Objectives and Approach
1. **IMU Denoising Modeling (IDM)**  
   Use neural networks to extract clean signals from noisy IMU data.  
2. **Masked IMU Modeling (MIM)**  
   Learn to recover masked IMU measurements (similar to BERT-style pretraining).  
3. **Autoregressive (AR) Method Exploration**  
   Investigate AR-based architectures to optimize denoising and prediction.  

### II. Progress and Challenges

#### 1. Literature Review
- **Key Paper**: [1] proposes a self-supervised denoising method with:  
  - Novel loss functions for noise reduction  
  - Training strategies without clean reference data  
- **Challenges**:  
  ❗ Complex mathematical derivations in the paper require code-level understanding (ongoing).  

#### 2. Code Reproduction (IMUDB Project)  
- **Goal**: Reproduce the official implementation  
- **Issues**:  
  ❗ Dataset too large for local download  
  ❗ Server login failures; partial reproduction with subset data failed  
- **Current Status**:  
  ⏸️ Paused due to data limitations; shifted focus to AR methods.  

#### 3. Autoregressive Method Experiments  
- **Reference Codebases**:  
  - [AR-Net](https://github.com/ourownstory/AR-Net)  
  - [auto-regressive-time-series-model](https://github.com/bhattbhavesh91/auto-regressive-time-series-model?tab=readme-ov-file)  
  - [DSARF](https://github.com/ostadabbas/DSARF?tab=readme-ov-file)  
- **Explorations**:  
  1. Apply AR models for IMU sequence prediction  
  2. Integrate temporal modeling into denoising pipelines  
- **Challenges**:  
  ❗ Unclear how to adapt AR methods for IMU-specific noise patterns  
  ❗ Implementation complexity exceeds current progress  
