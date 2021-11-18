## Image Captioning for Detection of Anomalous Situations

## 1. Training parameters and results (MSCOCO + AD dataset)
| Model & Config | Argmax | BEAM Search |
| :--- | :--- | :--- |
| **InceptionV3** <ul><li>Epochs = 13</li><li>Batch Size = 32</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.4050</li><li>val_loss: 3.0527</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.596818</li><li>BLEU-2: 0.356009</li><li>BLEU-3: 0.252489</li><li>BLEU-4: 0.129536</li></ul> |<ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.606086</li><li>BLEU-2: 0.359171</li><li>BLEU-3: 0.249124</li><li>BLEU-4: 0.126599</li></ul> |
| **InceptionV3** <ul><li>Epochs = 11</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.5254</li><li>val_loss: 3.1769</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.601791</li><li>BLEU-2: 0.344289</li><li>BLEU-3: 0.230025</li><li>BLEU-4: 0.108898</li></ul> |<ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.605097</li><li>BLEU-2: 0.356094</li><li>BLEU-3: 0.251132</li><li>BLEU-4: 0.129900</li></ul> |
| **InceptionV3** <ul><li>Epochs = 18</li><li>Batch Size = 128</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.2880</li><li>val_loss: 3.1889</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.596655</li><li>BLEU-2: 0.342127</li><li>BLEU-3: 0.229676</li><li>BLEU-4: 0.108707</li></ul> | <ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.593876</li><li>BLEU-2: 0.348569</li><li>BLEU-3: 0.242063</li><li>BLEU-4: 0.123221</li></ul> |
| **VGG16** <ul><li>Epochs = 7</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.6297</li><li>val_loss: 3.3486</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.557626</li><li>BLEU-2: 0.317652</li><li>BLEU-3: 0.216636</li><li>BLEU-4: 0.105288</li></ul> |<ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.568993</li><li>BLEU-2: 0.326569</li><li>BLEU-3: 0.226629</li><li>BLEU-4: 0.113102</li></ul> |
| **VGG16** <ul><li>Epochs = 7</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.6297</li><li>val_loss: 3.3486</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.557626</li><li>BLEU-2: 0.317652</li><li>BLEU-3: 0.216636</li><li>BLEU-4: 0.105288</li></ul> |<ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.568993</li><li>BLEU-2: 0.326569</li><li>BLEU-3: 0.226629</li><li>BLEU-4: 0.113102</li></ul> |
| **VGG16** <ul><li>Epochs = 7</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 2.6297</li><li>val_loss: 3.3486</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.557626</li><li>BLEU-2: 0.317652</li><li>BLEU-3: 0.216636</li><li>BLEU-4: 0.105288</li></ul> |<ul>**k = 3**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.568993</li><li>BLEU-2: 0.326569</li><li>BLEU-3: 0.226629</li><li>BLEU-4: 0.113102</li></ul> |

## 2. Project Pipeline

The project pipeline can be briefly summarized in the following four steps:

* Data Understanding: Here, you need to load the data and understand the representation 
* Data preprocessing: In this step, you will process both images & captions to the desired format.
* Train/Test Split: Combine both images & captions to create the train & test dataset.
* Model-Building: This is the stage where you will create your image captioning model by building Encoder , Attention & Decoder model
* Model Evaluation: Evaluate the model using greedy search, Beam Search, BLEU score and METEOR score


## 3. References
<ul type="square">
	<li><a href="https://arxiv.org/pdf/1502.03044v3.pdf">Show, Attend and Tell: Neural Image Caption
Generation with Visual Attention</a> - Kelvin Xu, Jimmy Ba, Ryan Kiros, Kyunghyun Cho, Aaron Courville, Ruslan Salakhutdinov, Richard Zemel, Yoshua Bengio</li>
	<li><a href="https://arxiv.org/pdf/1711.02578.pdf">Image Captioning and Classification of Dangerous Situations</a> - Octavio Arriaga, Paul Plöger, Matias Valdenegro-Toro</li>
</ul>
