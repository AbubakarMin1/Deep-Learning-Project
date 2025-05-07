# Deep-Learning-Project  
**Improving Detection Using MegaDetector and Advanced Camouflaged Object Detection Techniques**  

This project focuses on improving the accuracy of wildlife monitoring systems by enhancing the detection and classification of camouflaged animals in camera trap imagery. Specifically, it aims to integrate state-of-the-art Camouflaged Object Detection (COD) techniques with the existing MegaDetector to improve the detection of snow leopards, which tend to blend into complex natural backgrounds, especially in snowy environments.

## Project Overview
### Problem Statement  
The primary goal of this project is to enhance the existing MegaDetector model, which has been trained on ideal images and struggles with real-world images, particularly those taken in the Margalla area where snow leopards can be camouflaged by snow. Our solution aims to address the challenges posed by camouflaged images and improve classification accuracy.

### Approach  
- **MegaDetector**: We use the MegaDetector for animal detection in camera trap images.
- **Camouflaged Object Detection (COD)**: COD techniques such as **MIF-NET**, **R2CNet**, and **AGLNet** are integrated to refine the detection process and improve accuracy for challenging images.
- **AI4GAmazonRainforest Classifier**: Once improved by COD techniques, the detected images are passed onto the classifier for animal classification.

## Deliverables  
The project is structured around multiple deliverables, each addressing different aspects of the model improvement process.

### Deliverables
1. **Group 12 Presentation** - A summary of the overall approach, methodology, and progress of the project.  
2. **Group 12 Report** - A detailed report documenting the methods, experiments, and results achieved.  
3. **Download LILA Subset** - This file includes the data used for training.  
4. **MegaDetector Evaluation on COD10K** - The evaluation of MegaDetector’s performance on the COD10K dataset.  
5. **Training Approach to MegaDetector** - Details on how the MegaDetector was fine-tuned to handle camouflaged images.  
6. **Training on COD10K** - Two iterations of training the model on the COD10K dataset for better camouflaged object detection.

## Methodology  
### Camouflaged Object Detection Models:
- **MIF-NET**: A dual-branch mixture convolution model that enhances feature representation by expanding the receptive field.  
- **R2CNet**: A model that integrates dual-source information fusion for accurate detection of camouflaged objects.  
- **AGLNet**: A unified framework that integrates multiple auxiliary cues (e.g., texture, edge) to improve detection and segmentation accuracy.

These models will be tested on images taken from real-world scenarios to assess their ability to handle complex backgrounds and low-contrast environments, typical of snow leopard habitats.

## Files Structure
- **Deliverables**: Contains all deliverables for the project, organized by specific tasks.
  - **Deliverable-1**: Presentation and final report.
  - **Deliverable-2**: Group presentation and training-related files.
  - **Deliverable-3**: Download data and evaluation scripts.
  - **Deliverable-4**: Training scripts for MegaDetector.
  - **Deliverable-5**: Additional training scripts for improved detection.
- **LICENSE**: The licensing information for the project.  
- **README.md**: This file.

## Google Drive Link
For the latest IPython Notebooks used to visualize the data before training the model, after training the model, and during training, please refer to the [Google Drive folder](https://drive.google.com/drive/folders/1ecU6qbXc4-otjxU5pCZs2M4cwwH4Ac2n?usp=sharing).

## References
- [Pytorch Wildlife and Microsoft CameraTraps Repository](https://github.com/microsoft/CameraTraps)
- **MIF-NET**: [A Holistically Point-guided Text Framework for Weakly-Supervised Camouflaged Object Detection](https://arxiv.org/pdf/2501.06038)
- **R2CNet**: [Towards Accurate Camouflaged Object Detection with Mixture Convolution and Interactive Fusion](https://arxiv.org/pdf/2101.05687)
- **AGLNet**: [Adaptive Guidance Learning for Camouflaged Object Detection](https://arxiv.org/pdf/2405.02824)
