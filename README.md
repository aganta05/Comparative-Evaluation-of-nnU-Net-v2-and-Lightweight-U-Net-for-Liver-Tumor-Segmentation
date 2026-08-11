Tumor segmentation from computed tomography (CT) images plays a critical role in clinical diagnosis,
treatment planning, radiotherapy guidance, and disease progress monitoring (Sun et al., 2019). An
accurate delineation of tumor boundaries enables quantitative assessment of tumor progression
and supports personalized cure strategies (Akakuru et al., 2022). However, manual segmentation
by radiologists is labor-intensive, time-consuming, and an observer variant, and so motivates the
development of automated segmentation methods (Nair et al., 2025).
Despite recent advances in medical image analysis, accurate and reliable tumor segmentation in CT
scans remains challenging due to heterogeneity in tumor morphology, low contrast between tumor
and surrounding tissues, imaging artifacts, inter-subject variability (Abdoli et al., 2026). In addition,
some tumors may exhibit complex shapes and multi-scale spatial characteristics, making robust
feature extractions difficult for conventional approaches (Abdusalamalov et al., 2023).
Deep learning-based segmentation frameworks, particularly convolutional neural networks (CNNs),
have demonstrated strong performance in medical image segmentation tasks (Mienye et al., 2025).
Architectures such as U-Net and its variants have become widely adopted due to their encoder-decoder
structure and ability to capture contextual information (Yin et al., 2022) More recently, transformer-
based and hybrid CNN-transformer models have further improved segmentation performance by
modeling long-range spatial dependencies and multi-scale representations (Yousaf et al., 2026).
Although recent deep learning frameworks have achieved strong segmentation performance, many
state-of-the-art models require substantial computational resources and long training times. In
practical settings, lightweight architecture will offer advantages in terms of efficiency, interpretability,
and ease of deployment while still achieving competitive segmentation performance (Rasheed, 2026).
Motivated by this tradeoff, our work focuses on comparing a strong existing segmentation framework
with simpler custom-designed architectures for liver tumor segmentation in CT images.
In this work, we first utilized nnU-Net to perform supervised semantic segmentation on CT scans of
the liver, with the purpose of segmenting tumors. We began by following nnU-Net’s preprocessing
pipeline, followed by using a 3D nnU-Net with 5-fold cross validation. We analyzed its performance
and compared it with that of our customized lightweight 2D segmentation architecture based on an
encoder-decoder U-Net Design with skip connections. The custom model processes individual 2D
axial CT slices to reduce memory usage and training time. These 2D slice segmentation were stacked
to find the volume.
