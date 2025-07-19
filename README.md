# Background-Remover
Removing the background given an image. In this case, an object of interest is defined as the foreground object


<div style="display: flex; gap: 10px;">
  <img src="assets/0b0bd753-3094-4d4d-a888-8125acebfca9.png" width="480" height="600" />
  <img src="assets/0b0bd753-3094-4d4d-a888-8125acebfca9_mask.png" width="480" height="600" />
</div>


<div style="display: flex; gap: 10px;">
  <img src="assets/0b042c603ed7f9ec8165a7544dd62624.png" width="480" height="600" />
  <img src="assets/0b042c603ed7f9ec8165a7544dd62624_mask.png" width="480" height="600" />
</div>

<div style="display: flex; gap: 10px;">
  <img src="assets/0c2b3e3ab26f374390c6ab3bc94262be.png" width="480" height="600" />
  <img src="assets/0c2b3e3ab26f374390c6ab3bc94262be_mask.png" width="480" height="600" />
</div>


## Techniqual Details

- **MVANet** model was fine-tuned on a custom training dataset
- Real images (1,000) + Synthetic images (3,000) were used to train the model
- Real product images were annotated using custom built annotation tool.

### Custom Annoation Tool

- Built using Gradio-UI
- **HQ-SAM** ( variant of Segment Anything Model ) is used as the main model for the segmentation
- Allow to highlight background keypoints and foreground keypoints in order to obtain accurate segmentation maks
- Binary masks or gray-scale masks can be saved

<img src="assets/custom_mask_annotation_tool.png" width="480" height="600" />