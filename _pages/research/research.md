---
title: "Research"
permalink: /research/
author_profile: true
---
## Surgical Navigation and Human-Robot Collaboration

### Vision-Guided Surgical Navigation for Pelvic Tumor Resections
I validated a vision-guided modular jig system that projects preoperatively planned osteotomy lines directly onto the surgical site for real-time intraoperative bone resection. The system achieved sub-millimeter resection accuracy in pelvic tumor cases, improving the surgeon's ability to replicate the preoperative plan and maintain adequate surgical margins.

<table style="height:auto; width:auto;" cellspacing="0" cellpadding="0">
  <tr>
    <td><img src="/research/assets/pelvic.png" width=auto height=auto alt="Vision-guided pelvic tumor resection system"></td>
  </tr>
</table>

**Publications:**
- **V. Danesh**, P. Arauz, M. Boroji, A. Zhu, M. Cottone, E. Gould, FA Khan, I. Kao, "[Improved Accuracy in Pelvic Tumor Resections Using a Real-Time Vision-Guided Surgical System](https://doi.org/10.1002/jor.26111)," *Journal of Orthopaedic Research*, 2025.
- G. He, **V. Danesh**, M. Boroji, A. Kermanian, P. Arauz, FA Khan, I. Kao, "[Real-Time, Vision-Guided Orthopedic Surgery for Wide Resection of Primary Bone Sarcomas](https://doi.org/10.1016/B978-0-443-13912-3.00033-6)," *Handbook of Robotic and Image-Guided Surgery*, pp. 633–644, Elsevier, 2026.

### Human-Robot Collaborative Resection Platform (Ongoing)
Building on vision-guided navigation, this work pairs the surgeon with a collaborative robotic platform for complex sarcoma resections. The resection plan is expressed mathematically and enforced by an admittance controller, while the surgeon leads the cut and retains full authority. The aim is to democratize high-quality sarcoma care across community hospitals that lack dedicated orthopedic oncology teams.

<hr>

## AI-Driven Optical Biopsy

### In-Vivo Raman Spectroscopy for Real-Time Skin Cancer Diagnosis (Ongoing)
Frozen section analysis is the current standard for intraoperative margin assessment, but it is slow, subjective, and not always available outside major cancer centers. This project develops a handheld in-vivo Raman spectroscopic probe paired with deep learning models to give surgeons objective, real-time tissue characterization at the point of care. Skin cancer is the first clinical target, with planned extension to sarcoma margin assessment.

The system collects molecular fingerprint data from tissue in seconds and returns a diagnostic readout alongside conventional pathology workflows. The goal is to reduce reliance on invasive biopsies and make optical biopsy practical in community hospitals and under-resourced regions.

**Related Presentations:**
- R. Basak, **V. Danesh**, M. Boroji, I. Kao, X. Qian, T. Zhang, et al., "[Skin Lesion Subtype Classification Using Lesion and Border Radiomic Features](https://aapm.confex.com/aapm/2025am/meetingapp.cgi/Paper/19470)," *AAPM 67th Annual Meeting*, 2025.
- M. Boroji, **V. Danesh**, P. Prasanna, J. Kim, X. Qian, M. Khari, et al., "[Convolutional Neural Network Attention-Guided Segmentation to More Accurately Identify the Edges of Benign and Malignant Skin Tumors](https://aapm.confex.com/aapm/2024am/meetingapp.cgi/Paper/13085)," *AAPM 66th Annual Meeting*, 2024.

<hr>

### Ex-Vivo Raman Spectroscopy and AI-Based Classification of Soft Tissue Sarcomas
I led model development and training for a PyTorch ResNet pipeline that classifies soft tissue sarcomas from Raman spectra. We designed a preprocessing, denoising, and classification framework for 286,672 spectra from seven patients, achieving 97.1% accuracy across eight tissue types. A clinical alert metric yielded a 1.46% malignant misclassification rate—supporting Raman spectroscopy as a fast, non-invasive alternative to conventional margin assessment.

<table style="height:auto; width:auto;" cellspacing="0" cellpadding="0">
  <tr>
    <td><img src="/research/assets/average_spectra.png" width=auto height=auto alt="Average Raman spectra by tissue type"></td>
    <td><img src="/research/assets/cnn.png" width=auto height=auto alt="CNN architecture"></td>
  </tr>
</table>
<center>
  <img src="/research/assets/eval.png" width=auto height=auto alt="Classification evaluation results">
</center>

**Publication:**
- M. Boroji†, **V. Danesh**†, D. Barrera, E. Lee, PG Arauz, RF Farrell, et al., "[Ex-vivo Raman Spectroscopy and AI-Based Classification of Soft Tissue Sarcomas](https://doi.org/10.1371/journal.pone.0330618)," *PLoS ONE*, 20(9), e0330618, 2025.

<hr>



## Robotic Manipulation

### Motion Planning for Object Manipulation by Edge-Rolling
A common strategy for manipulating heavy objects is to keep at least one point of the object in contact with the environment. For cylindrical or curved-edge objects, rolling along the edge can meet this constraint with greater efficiency and maneuverability than sliding or pivoting alone.

We developed a screw-theory-based approach that approximates prehensile edge-rolling motion on arbitrary paths as a sequence of constant screw displacements. A task-space planner generates paths between two configurations through rolling and pivoting motions while respecting joint limits. We validated the approach with the Franka Emika Panda, manipulating a cylinder along both linear and curved paths.

<table style="height:auto; width:auto;" cellspacing="0" cellpadding="0">
  <tr>
    <td><img src="/research/assets/EdgeRolling.png" width=480 height=360 alt="Edge-rolling manipulation concept"></td>
    <td><img src="/research/assets/EdgeRolling_BackAndForthPath.gif" width=auto height=auto alt="Cylinder manipulation along a back-and-forth path"></td>
    <td><img src="/research/assets/EdgeRolling_FullCirclePath.gif" width=auto height=auto alt="Cylinder manipulation along a full circle path"></td>
  </tr>
</table>

**Publication:**
- M. Boroji†, **V. Danesh**†, I. Kao, A. Fakhari, "[Motion Planning for Object Manipulation by Edge-Rolling](https://doi.org/10.1109/IROS58592.2024.10802581)," *IEEE/RSJ IROS*, 2024.

<hr>

### [PandaSim](/pandaSim/): Physics-Based Dexterous Manipulation with Screw Motion Planning
I developed a complete manipulation pipeline in the Genesis physics-based simulator using a Franka Emika Panda robot. The system integrates geometry extraction, screw motion planning, and resolved-rate motion control. Finger-level rotational degrees of freedom enhance dexterity, achieving a 96% object reorientation success rate. See the [full project page](/pandaSim/) or [GitHub repository](https://github.com/VahidDanesh/pandaSim).

<table style="height:auto; width:auto;" cellspacing="0" cellpadding="0">
  <tr>
    <td><img src="/research/assets/v1.gif" height="250" alt="Object reorientation in PandaSim"></td>
    <td><img src="/research/assets/v4.gif" height="250" alt="Object reorientation in PandaSim"></td>
  </tr>
</table>
