# Cross-Layer-Autonomous-Cybersecurity-Framework
This repository includes code for the paper "Towards Zero Touch Networks: Cross-Layer Automated Security Solutions for 6G Wireless Networks" accepted and to appear in IEEE Transactions on Communications (TCOM), focusing on autonomous cybersecurity (physical-layer authentication and cross-layer intrusion detection system development) using AutoML techniques.

The paper is publicly available on TechRxiv: [Towards Zero Touch Networks: Cross-Layer Automated Security Solutions for 6G Wireless Networks](https://d197for5662m48.cloudfront.net/documents/publicationstatus/171667/preprint_pdf/557ec6745a4fe6fabc76c5e4d764d602.pdf)
  
- This code is an implementation of the major components of the proposed AutoML framework in the paper, which consists of:
   * Including **automated data pre-processing (mainly data balancing), automated feature engineering, automated model selection, hyperparameter optimization, and automated model updating** (concept drift adaptation).
   * For physical-layer authentication and intrusion detection system development in dynamic networking environments.

This code is also part of a series of GitHub repositories related to Zero-Touch Networks (ZTNs), autonomous cybersecurity, network automation, and AutoML:  
1. [AutoML-Implementation-for-Static-and-Dynamic-Data-Analytics](https://github.com/Western-OC2-Lab/AutoML-Implementation-for-Static-and-Dynamic-Data-Analytics)  
2. [AutoML-and-Adversarial-Attack-Defense-for-Zero-Touch-Network-Security](https://github.com/Western-OC2-Lab/AutoML-and-Adversarial-Attack-Defense-for-Zero-Touch-Network-Security)
3. [AutonomousCyber-AutoML-based-Autonomous-Intrusion-Detection-System](https://github.com/Western-OC2-Lab/AutonomousCyber-AutoML-based-Autonomous-Intrusion-Detection-System)

## Abstract of The Paper
The transition from fifth-generation (5G) to sixth-generation (6G) mobile networks necessitates network automation to meet the escalating demands for high data rates, ultra-low latency, and integrated technology. Recently, Zero-Touch Networks (ZTNs), driven by Artificial Intelligence (AI) and Machine Learning (ML), are designed to automate the entire lifecycle of network operations with minimal human intervention, presenting a promising solution for enhancing automation in 5G/6G networks. However, the implementation of ZTNs brings forth the need for autonomous and robust cybersecurity solutions, as ZTNs rely heavily on automation. AI/ML algorithms are widely used to develop cybersecurity mechanisms, but require substantial specialized expertise and encounter model drift issues, posing significant challenges in developing autonomous cybersecurity measures. Therefore, this paper proposes an automated security framework targeting Physical Layer Authentication (PLA) and Cross-Layer Intrusion Detection Systems (CLIDS) to address security concerns at multiple Internet protocol layers. The proposed framework employs drift-adaptive online learning techniques and a novel enhanced Successive Halving (SH)-based Automated ML (AutoML) method to automatically generate optimized ML models for dynamic networking environments. Experimental results illustrate that the proposed framework achieves high performance on the public Radio Frequency (RF) fingerprinting and the Canadian Institute for Cybersecurity Intrusion Detection System 2017 (CICIDS2017) datasets, showcasing its effectiveness in addressing PLA and CLIDS tasks within dynamic and complex networking environments. Furthermore, the paper explores open challenges and research directions in the 5G/6G cybersecurity domain. This framework represents a significant advancement towards fully autonomous and secure 6G networks, paving the way for future innovations in network automation and cybersecurity.

## Concept Drift
In non-stationary and dynamic networking environments, the distribution of input data often changes over time, known as concept drift. The occurrence of concept drift will result in the performance degradation of the current trained data analytics model. Traditional offline machine learning (ML) models cannot deal with concept drift, making it necessary to develop online adaptive analytics models that can adapt to the predictable and unpredictable changes in data streams. 

To address concept drift, effective methods should be able to detect concept drift and adapt to the changes accordingly. Therefore, concept drift detection and adaptation are the two major steps for online learning on data streams.

## Implementation 
<p float="left">
  <img src="https://github.com/Western-OC2-Lab/Cross-Layer-Autonomous-Cybersecurity-Framework/blob/main/Framework.jpg" width="1000" />
</p>

### Tasks
- Physical-Layer Authentication (PLA)
- Intrusion Detection System (IDS)
### Steps
1. Automated Data Pre-Processing
   * Data Balancing
2. Automated Feature Engineering
   * Drift-based Dynamic Feature Selection: PCC-based Select-K-Best
3. Combined Algorithm Selection and Hyper-parameter optimization (CASH)
   * Online Base Model Learning
   * Concept Drift Detection
   * Automated Model Selection
   * Hyperparameter Optimization
   * Successive Halving (SH)-based CASH Method

### Online Learning/Concept Drift Adaptation Algorithms  
* Adaptive Random Forest (ARF) 
* Streaming Random Patches (SRP)
* Hoeffding Trees (HT)
* Hoeffding Adaptive Tree (HAT)
* Extremely Fast Decision Tree (EFDT)
* Aggregated Mondrian Forest (AMF)
* Leveraging Bagging (LB)
* SH-CASH Method
  * Proposed in this work

### Drift Detection Algorithms
* Adaptive Windowing (ADWIN)
* Early Drift Detection Method (EDDM)

### Datasets 
1. Oracle Radio Frequency (RF) fingerprinting dataset, a public dataset for physical layer authentication (PLA)
   * Publicly available at: https://www.genesys-lab.org/oracle
2. CICIDS2017 dataset, a popular network traffic dataset for intrusion detection problems
   * Publicly available at: https://www.unb.ca/cic/datasets/ids-2017.html

### Requirements  
* Python 3.6+ 
* [scikit-learn](https://scikit-learn.org/stable/)  
* [River](https://riverml.xyz/dev/)

## Contact-Info
Please feel free to contact me for any questions or cooperation opportunities. I'd be happy to help.
* Email: [liyanghart@gmail.com](mailto:liyanghart@gmail.com)
* GitHub: [LiYangHart](https://github.com/LiYangHart) and [Western OC2 Lab](https://github.com/Western-OC2-Lab/)
* LinkedIn: [Li Yang](https://www.linkedin.com/in/li-yang-phd-65a190176/)  
* Google Scholar: [Li Yang](https://scholar.google.com.eg/citations?user=XEfM7bIAAAAJ&hl=en)

## Citation
If you find this repository useful in your research, please cite this article as:  

L. Yang, S. Naser, A. Shami, S. Muhaidat, L. Ong, and M. Debbah, "Towards zero-touch networks: Cross-layer automated security solutions for 6G wireless networks," *IEEE Transactions on Communications*, pp. 1–30, 2025. 

```
@article{Yang23971707,
author = {Yang, Li and Naser, Shimaa and Shami, Abdallah and Muhaidat, Sami and Ong, Lyndon and Debbah, Merouane},
title = {Towards Zero Touch Networks: Cross-Layer Automated Security Solutions for 6G Wireless Networks},
doi = {},
journal = {IEEE Transactions on Communications},
pages = {1--30},
url = {https://doi.org/10.36227/techrxiv.23971707.v1},
year = {2025}
}
```
