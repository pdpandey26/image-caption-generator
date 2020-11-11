#### Abstract
Image captioning is a very interesting problem in machine learning. With the development of deep neural network, deep learning approach is the state of the art of this problem. The main mission of image captioning is to automatically generate an image's description, which requires our understanding about content of images. The main idea of this model is separate CNN and RNN, with only merge their ouput at the end and predicted by softmax layer. Base on it, we develop the model to generate image caption. 

### I. Main Idea:
* Combine ConvNet with LSTM
* Deep ConvNet as image encoder
* Language LSTM as text encoder
* Fully connected layer as decoder
* End-to-end model I -> S
* Maximize P(S|I)

### II. Dataset: 
[Flickr 8k](https://forms.illinois.edu/sec/1713398), train/val/test 6:1:1.

The definitive description of the dataset is in the paper “Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics” from 2013.

The authors describe the dataset as follows:

*"We introduce a new benchmark collection for sentence-based image description and search, consisting of 8,000 images that are each paired with five different captions which provide clear descriptions of the salient entities and events … The images were chosen from six different Flickr groups, and tend not to contain any well-known people or locations, but were manually selected to depict a variety of scenes and situations."*

— [Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics, 2013](https://jair.org/index.php/jair/article/view/10833/25854).

### III. Baseline Model:

<p align="center">
  <img src="https://i.imgur.com/rDGYTBH.png" />
</p>

### V. Tuning hyperparameters:
> ### Encoder ConvNet:
* VGG16
* **Resnet50**
* Densenet121
* Inceptionv3

> ### Optimizer
* **Adam**: 
* Nadam: 
* RMSprop: 
* Sgd:

### VI. Evaluation and result:
> **We use BLEU-score which is evaluate metric:**
+ BLEU-1: 0.542805
+ BLEU-2: 0.301714
+ BLEU-3: 0.207351
+ BLEU-4: 0.095704

> **Caption of new images:**
<p align="center">
  <img src="https://i.imgur.com/uFE7Hkn.png" />
</p>
