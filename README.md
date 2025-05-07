# Deep-Learning-Project  
**Improving Detection Using MegaDetector and Advanced Camouflaged Object Detection Techniques**  

This project focuses on improving the accuracy of wildlife monitoring systems by enhancing the detection of camouflaged animals in camera trap imagery. Specifically, it aims to integrate state-of-the-art Camouflaged Object Detection (COD) techniques with the existing MegaDetector to improve the detection of animals, which tend to blend into complex natural backgrounds.

## Project Overview
### Problem Statement  
The primary goal of this project is to enhance the existing MegaDetector model, which has been trained on ideal images and struggles with real-world images, particularly those taken in the Margalla area where snow leopards can be camouflaged by snow. Our solution aims to address the challenges posed by camouflaged images and improve detection accuracy.

### Approach  
- **MegaDetector**: We use the MegaDetector for animal detection in camera trap images.
- **Camouflaged Object Detection (COD)**: Training on the COD10k Dataset, which mainly contains camoflaged animal images and we trained it to detect the animals given the bounding boxes to refine the detection process and improve accuracy for challenging images.

## Deliverables  
The project is structured around multiple deliverables, each addressing different aspects of the model improvement process.

### Deliverables
1. **Group 12 Presentation** - A summary of the initial approach which revolved around using models like MIF-net and R2CNet, but we ultimately had to remove them because the scope of the project changed as they were trained on COD10k dataset (initially we were working to resolve issues around camera trap picture).
2. **Group 12 Report** - A detailed report documenting the methods, experiments, and general Literature Reveiw of Wildlife monitoring, discussion about Pytorch Wildlife, Models to be used in Camoflaged object detection (models were not used, due to change in scope)
3. **Group_12.ipynb** - Our first try at getting the Lila dataset, it wasn't successful because the annotation and metadata files alone for that dataset were huge and we couldn't process the scripts on either kaggle or google collabs
4. **Download LILA Subset** - This is the follow up file to download the Lila dataset, we used chunking to download and extract the tuples related to the species we were extracting (species_of_interest = ['leopard','snow leopard','leopardus']) and after generating chunks that could fit in the RAM+Virtual Memory, we concetanted the chunks and then did the lookup for the images, it worked.
5. **MegaDetector Evaluation on COD10K** - The evaluation of MegaDetector’s performance on the COD10K dataset.  (Rayed)
6. **Training Approach to MegaDetector** - Details on how the MegaDetector was to be fine-tuned to handle camouflaged images, wasnt executed due to logistical issues related mostly to LUMS internet.  
7. **Training on COD10K** - Two iterations of training the model on the COD10K dataset for better camouflaged object detection, the 1st file is training primarily to get weights of that model and just to test how things would be planned, the second one was a little bit more refined but only ran till 8 epochs due to logistical limitations.

## Research before the scope was changed
### Camouflaged Object Detection Models:
- **MIF-NET**: A dual-branch mixture convolution model that enhances feature representation by expanding the receptive field.  
- **R2CNet**: A model that integrates dual-source information fusion for accurate detection of camouflaged objects.  
- **AGLNet**: A unified framework that integrates multiple auxiliary cues (e.g., texture, edge) to improve detection and segmentation accuracy.

These models will be tested on images taken from real-world scenarios(CameraTrap Images) to assess their ability to handle complex backgrounds and low-contrast environments, typical of snow leopard habitats.

## Files Structure
- **Deliverables**: Contains all deliverables for the project, organized by specific tasks.
  - **Deliverable-1**: Presentation and report (Initial Scope and Literature review).
  - **Deliverable-2**: Trying to get Dataset.
  - **Deliverable-3**: Forward Pass and Getting Lila dataset.
  - **Deliverable-4**: Training scripts for MegaDetector.
  - **Deliverable-5**: Additional training scripts for improved detection.
- **Latest**:
  - **training-md.ipynb**: Training file to 40 epochs with the COD10k dataset
  - **visualizing-the-baseline-detections.ipynb**: Baseline model (Megadetector: MDV6-yolov10-c) and its visualizations for comparison
  - **visualizing-the-results.ipynb**: Trained model and its visualizations
- **LICENSE**: The licensing information for the project.  
- **README.md**: This file.

## Google Drive Link
For the latest IPython Notebooks used to visualize the data before and after training the model, please refer to the [Google Drive folder](https://drive.google.com/drive/folders/1ecU6qbXc4-otjxU5pCZs2M4cwwH4Ac2n?usp=sharing).

## References
- [Pytorch Wildlife and Microsoft CameraTraps Repository](https://github.com/microsoft/CameraTraps)
- **MIF-NET**: [A Holistically Point-guided Text Framework for Weakly-Supervised Camouflaged Object Detection](https://arxiv.org/pdf/2501.06038)
- **R2CNet**: [Towards Accurate Camouflaged Object Detection with Mixture Convolution and Interactive Fusion](https://arxiv.org/pdf/2101.05687)
- **AGLNet**: [Adaptive Guidance Learning for Camouflaged Object Detection](https://arxiv.org/pdf/2405.02824)
