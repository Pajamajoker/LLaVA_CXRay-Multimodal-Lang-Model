
# LLaVA CXRay Model Reseasrch PRoject 
### Multimodal Large Language Model Fine-Tuned for Chest X-ray Images

LLaVA CXRay is a multimodal large language model designed for generating radiology reports from chest X-ray images.

You can test and Chest X rays with just these lines of code. 

(NVIDIA GPU VRAM>16GB neeeded)
```python
from transformers import AutoModel
from PIL import Image
model = AutoModel.from_pretrained("ECOFRI/CXR-LLAVA-v2", trust_remote_code=True)
model = model.to("cuda")
cxr_image = Image.open("img.jpg")
response = model.write_radiologic_report(cxr_image)
```
 > The radiologic report reveals a large consolidation in the right upper lobe of the lungs. There is no evidence of pleural effusion or pneumothorax. The cardiac and mediastinal contours are normal. 


### Install Dependencies
Make sure you have PyTorch installed. After that, you can install the additional required dependencies. Run the command in your terminal:
```python
pip install transformers sentencepiece protobuf pillow
```

### NOTE & DISCLAIMER!!
The repo and contents is still under research actively. Please do not use this code for anything other than testing and research purposes!

