# ACNE04 Dataset Balancing – Synthetic Image Supplement

This repository provides access to a set of **synthetic acne images** generated using the **ACNEDIT** pipeline. These images were created to **balance the distribution of severity levels** in the **ACNE04 dataset**, improving the performance and fairness of acne classification models.

## 🔍 Motivation

The original ACNE04 dataset has an **imbalanced distribution** of acne severity levels, which may bias learning algorithms. To address this, we generated additional samples for the underrepresented categories (`severe` and `very severe`) using our realistic acne synthesis approach.

![Example](https://github.com/user-attachments/assets/9c7df5cc-d5c0-4a54-b5f0-e1ced61af096)

## 📊 Severity Distribution

| Severity Level | Label  | Original Count | Generated | Total After Balancing |
|----------------|--------|----------------|-----------|------------------------|
| Mild           | levle0 | 513            | 0         | 513                    |
| Moderate       | levle1 | 633            | 0         | 633                    |
| Severe         | levle2 | 182            | 218       | 400                    |
| Very Severe    | levle3 | 129            | 271       | 400                    |

## 📁 Download

You can download the generated images for the `severe` and `very severe` classes from the following link:

🔗 **[Download Synthetic Images](https://drive.google.com/drive/folders/1A4bCGSCOWIjHkfEGRumhQwsZWQXaM_EQ?usp=sharing)**  

## 🧪 Notes

- All synthetic images were generated using **real facial data** with **locally applied acne edits** to preserve realism.
- Images are in `.jpg` format and organized by severity label (`levle2_generated/` and `levle3_generated/` folders).
- File names are anonymized and do not overlap with the original ACNE04 dataset.

## 📄 Citation
If you use these images in your research, please cite our work (anonymized for the moment).
We also thank Wu et al. for providing the ACNE04 dataset, which served as a foundation for this work. 

