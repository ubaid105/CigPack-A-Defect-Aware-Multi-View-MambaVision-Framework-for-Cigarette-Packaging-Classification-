# CigPack-A-Defect-Aware-Multi-View-MambaVision-Framework-for-Cigarette-Packaging-Classification-

# Abstract
This repository presents a multi-view deep learning framework for automated cigarette packaging quality classification using the CPQ-36K dataset. The proposed approach integrates a shared MambaVision backbone with Defect-Aware Cross-View Attention (DACVA), Adaptive Cross-View Feature Fusion (ACVFF), and Hard Example Contrastive Learning (HECL) to classify packages into Good, Damaged, and Deformed categories. The reported experimental results achieve 88.35% classification accuracy and an F1-score of 89.14%.

# Introduction
Conventional single-view inspection methods may overlook defects that are visible only from other viewpoints. This project addresses this limitation by exploiting six synchronized views of each cigarette package. The proposed framework models defect-related dependencies, adaptively fuses informative views, and improves discrimination between visually similar packaging defects.

# Dataset Preprocessing
The CPQ-36K dataset contains real-world cigarette packaging images captured from Front, Back, Left, Right, Top, and Bottom viewpoints. Preprocessing includes image resizing to 224 × 224 pixels, pixel normalization, removal of corrupted images, and data augmentation through random rotations, flipping, and scaling. The dataset is divided into training, validation, and testing subsets using a 70:15:15 ratio, with all six views of each physical package kept within the same subset to prevent data leakage.

# Training of the Proposed Model
The model processes six synchronized images using a shared MambaVision backbone. DACVA enhances defect-aware cross-view representations, ACVFF assigns adaptive weights based on view reliability and defect informativeness, and HECL improves feature discrimination through hard-example contrastive learning. The classification head predicts the final packaging-quality category, while training jointly optimizes cross-entropy and HECL losses.

# Python
The proposed framework is implemented in Python using PyTorch for deep learning and GPU acceleration. The main dependencies include MambaVision, TorchVision, NumPy, OpenCV, Pillow, scikit-learn, Matplotlib, Seaborn, and tqdm. A compatible NVIDIA GPU and CUDA-enabled PyTorch installation are recommended for model training.

# Others (Unofficial)
Swift (iOS): SwiftyOpenTC Java: opentc4j Android: android-opentc PHP: opentc4php Pure JavaScript: opentc-js WebAssembly: wasm-opentc
