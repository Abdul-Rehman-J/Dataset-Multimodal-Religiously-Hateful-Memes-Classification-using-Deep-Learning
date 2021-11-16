# Multimodal Religiously Hateful Memes

This repo contains the ***dataset*** for _Multimodal-Religiously-Hateful-Memes-Classification-using-Deep-Learning_

# The Religiously Hateful Memes 

The spread of hateful content, especially toward religious entities, is increasing on social media. Memes are one of the widely adopted modes of communication on social media platforms like Facebook, Twitter, Reddit, and Instagram. Religious hateful content has a greater negative impact on society. Detection of such content is very significant for maintaining platform neutrality. This dataset aims to drive progress in multimodal religiously hateful memes detection.



# Dataset details

The files for this folder are arranged as follows:

`/image`          -        contain images files  
`labels.jsonl`    -        the annotation file


>The `.jsonl` format contains one JSON-encoded example per line, each of which has the following fields:
- `text`        - the text in the meme
- `img`         - the path to `image/` directory
- `label`       - the label for meme (0=not-hateful, 1=hateful)


## Data distribution: 
Memes and Label (0=not-hateful, 1=hateful)

Dataset|1|0|Total
-------------|--------|--------|-----
religiously hateful memes|1020|980|2000

# Results 
We use the pytorch based [Facebook MMF](https://github.com/facebookresearch/mmf) framework for training. For image feature are extracted via [vqa-maskrcnn-benchmark](https://github.com/facebookresearch/mmf/blob/master/tools/scripts/features/extract_features_vmb.py).

The feature extrated using our dataset is available [here](https://drive.google.com/drive/folders/1lj8Bzm993rI28DLzamEtO8a2xvAKlP3T?usp=sharing)

# Model
Model performances comparison with baseline [VisualBERT](https://github.com/uclanlp/visualbert) model pre-trained on [Conceptual caption (CC)](https://github.com/google-research-datasets/conceptual-captions) dataset.


Type|Model|Accuracy|AUROC 
-------------|--------|--------|--------
Baseline |VisualBERT CC ID=_60_ |70.93|75.21
Our |VisualBERT CC  |**70.60**|**78.99**




> As per the size and content nature, some examples, although very unlikely, may have been misclassified. As objectivity of individual annotators might have the slightest chance to vary their opinion on a particular label. 



# Citations
If you wish to cite this work, please use the following BiBTeX:

```

```

# Contact
If you have any questions or comments on the dataset, please contact abdulrehman.cs@au.edu.pk or one of the authors.
