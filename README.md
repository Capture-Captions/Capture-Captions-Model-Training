## Image Captioning for Detection of Anomalous Situations

## 1. Training parameters and results (MSCOCO + AD dataset)
| Model & Config | Argmax | BEAM Search |
| :--- | :--- | :--- |
| **InceptionV3** <ul><li>Epochs = 50</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.432</li><li>val_loss: 1.252</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.606818</li><li>BLEU-2: 0.356009</li><li>BLEU-3: 0.252489</li><li>BLEU-4: 0.129536</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.596086</li><li>BLEU-2: 0.359171</li><li>BLEU-3: 0.249124</li><li>BLEU-4: 0.126599</li></ul> |
| **InceptionV3** <ul><li>Epochs = 20</li><li>Batch Size = 32</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.497</li><li>val_loss: 1.578</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.400791</li><li>BLEU-2: 0.254289</li><li>BLEU-3: 0.150025</li><li>BLEU-4: 0.108898</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.415097</li><li>BLEU-2: 0.276094</li><li>BLEU-3: 0.171132</li><li>BLEU-4: 0.119900</li></ul> |
| **VGG16** <ul><li>Epochs = 50</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.410</li><li>val_loss: 1.002</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.677626</li><li>BLEU-2: 0.457652</li><li>BLEU-3: 0.286636</li><li>BLEU-4: 0.205288</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.648993</li><li>BLEU-2: 0.456569</li><li>BLEU-3: 0.276629</li><li>BLEU-4: 0.203102</li></ul> |
| **VGG16** <ul><li>Epochs = 20</li><li>Batch Size = 32</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.488</li><li>val_loss: 1.432</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.437626</li><li>BLEU-2: 0.317652</li><li>BLEU-3: 0.216636</li><li>BLEU-4: 0.155288</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.488993</li><li>BLEU-2: 0.326569</li><li>BLEU-3: 0.226629</li><li>BLEU-4: 0.153102</li></ul> |

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
	<li><a href="https://machinelearningmastery.com/calculate-bleu-score-for-text-python/">BLEU score</li>
	
</ul>
