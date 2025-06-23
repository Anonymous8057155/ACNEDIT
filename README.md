# ACNE04 Dataset Balancing – Synthetic Image Supplement

This repository provides access to a set of **synthetic acne images** generated using the **ACNEDIT** pipeline. These images were created to **balance the distribution of severity levels** in the **ACNE04 dataset**, improving the performance and fairness of acne classification models.

## 🔍 Motivation

The original ACNE04 dataset has an **imbalanced distribution** of acne severity levels, which may bias learning algorithms. To address this, we generated additional samples for the underrepresented categories (`severe` and `very severe`) using our realistic acne synthesis approach.

Below are examples of synthetic images generated for various acne severity levels, highlighting how our method augments underrepresented categories.
![Example](https://github.com/user-attachments/assets/9c7df5cc-d5c0-4a54-b5f0-e1ced61af096)

## 📊 Severity Distribution

| Severity Level | Label  | Original Count | Generated | Total After Balancing |
|----------------|--------|----------------|-----------|------------------------|
| Mild           | levle0 | 513            | 0         | 513                    |
| Moderate       | levle1 | 633            | 0         | 633                    |
| Severe         | levle2 | 182            | 218       | 400                    |
| Very Severe    | levle3 | 129            | 271       | 400                    |

## ⚙️ What is ACNEDIT?

In this work, we present ACNEDIT, a workflow based on Generative Adversarial Networks (GANs) designed to modify the severity of acne on facial images derived from user-provided selfies. ACNEDIT preserves realistic skin details and ensures coherence both among lesions and with the surrounding facial structure. ACNEDIT consists of three key stages:
1.  Precise analysis of the input image to detect and assess acne characteristics.
2.  Context-aware overlay of one or more acne lesions based on this analysis.
3.  Refinement of the augmented image using a LaMa-based model trained on the ACNE04 dataset, along with post-processing techniques to produce highly realistic results.

![workflow](https://github.com/user-attachments/assets/b28cee69-f017-4b69-b85f-29eb7cc43a4c)
**Figure 1:** Overview of ACNEDIT: a method for modifying severity of acne on any part of facial image.

The example below illustrates how ACNEDIT transforms a facial image by adding acne lesions at varying severity levels, in contrast to a LaMa-only inpainting baseline.

![sev_comparison](https://github.com/user-attachments/assets/937d6c68-4898-4fcd-80e3-f700bc6fc873)

**Figure 2:** From left to right: original input image, LaMa-only inpainting (low realism), and three ACNEDIT-generated outputs with increasing acne severity levels.

By leveraging lesion overlays and high-resolution full-face synthesis, ACNEDIT addresses the imbalance in the ACNE04 dataset by augmenting underrepresented severity categories, such as severe and very severe acne. This enhances model training by providing a more balanced and diverse dataset.

## 📁 Download

You can download the generated images for the `severe` and `very severe` classes from the following link:

🔗 **[Download Synthetic Images](https://drive.google.com/drive/folders/1A4bCGSCOWIjHkfEGRumhQwsZWQXaM_EQ?usp=sharing)**  

## 🧪 Notes

- All synthetic images were generated using **real facial data** from ACNE04 dataset with **locally applied acne edits** to preserve realism.
- Images are in `.jpg` format and organized by severity label (`levle2_generated/` and `levle3_generated/` folders).

## 📄 Citation
If you use these images in your research, please cite our work (anonymized for the moment).
We also thank Wu et al. for providing the ACNE04 dataset, which served as a foundation for this work. 

