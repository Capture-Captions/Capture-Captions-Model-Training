## Image Captioning for Detection of Anomalous Situations

## 1. Training parameters and results (MSCOCO + AD dataset)
| Model & Config | Argmax | BEAM Search |
| :--- | :--- | :--- |
| **InceptionV3** <ul><li>Epochs = 50</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.410</li><li>val_loss: 1.252</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.666818</li><li>BLEU-2: 0.456009</li><li>BLEU-3: 0.302489</li><li>BLEU-4: 0.209536</li><li>METEOR: 0.212134</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.596086</li><li>BLEU-2: 0.409171</li><li>BLEU-3: 0.249124</li><li>BLEU-4: 0.126599</li><li>METEOR: 0.163241</li></ul> |
| **Resnet50** <ul><li>Epochs = 50</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.415</li><li>val_loss: 1.358</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.647626</li><li>BLEU-2: 0.407652</li><li>BLEU-3: 0.286636</li><li>BLEU-4: 0.155288</li><li>METEOR: 0.157213</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.558993</li><li>BLEU-2: 0.356569</li><li>BLEU-3: 0.206629</li><li>BLEU-4: 0.053102</li><li>METEOR: 0.126754</li></ul> |
| **VGG16** <ul><li>Epochs = 50</li><li>Batch Size = 64</li><li>Optimizer = Adam</li></ul> |<ul>**Crossentropy loss**<br>*(Lower the better)*<li>loss(train_loss): 0.457</li><li>val_loss: 1.521</li>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.587525</li><li>BLEU-2: 0.357878</li><li>BLEU-3: 0.246454</li><li>BLEU-4: 0.105499</li><li>METEOR: 0.135288</li></ul> |<ul>**k = 5**<br><br>**BLEU Scores on Validation data**<br>*(Higher the better)*<li>BLEU-1: 0.538225</li><li>BLEU-2: 0.306479</li><li>BLEU-3: 0.206123</li><li>BLEU-4: 0.08120</li><li>METEOR: 0.095288</li></ul> |


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
