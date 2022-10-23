# Prompt-Engineering-for-Vision-Language-Models

Zero-shot learning models like CLIP leverage natural language text as supervisory signals unlike traditional supervised learning approaches. They show great performance gains over other approaches. However, given that the labels consist of natural text, the choice of words and phrases used becomes important. We present a novel topological based approach that allows us to select text prompts that are most representative of a classes. We rely on MAPPER, a topology preserving projection algorithm to construct a Reeb graph of the embedding space, and further propose a margin-based approach to select subgraphs that provide the greatest predictive value. We show empirical evidence of the efficacy of our algorithm on zero-shot classification for Imagenette, a subset of the large Imagenet dataset. Consequently, we also discuss on the use of topological methods to analyse the effect of synonyms and other hypernyms on the performance of CLIP. 


## CLIP MODEL
```
Input : Image + set of text labels for classes.
```
<img src="https://github.com/axit54/Prompt-Engineering-for-Vision-Language-Models/blob/main/images/clip.png">

## Proposed Algorithm
```
Standard Approach: Take a large set of prompts, use average embedding for 
					classification.

Problem!   Prompts may be misleading (E.g.: A sketch of {}, a tattoo of {}.

Use Mapper to find groups of prompts that have largest "margin".
```
<img src="https://github.com/axit54/Prompt-Engineering-for-Vision-Language-Models/blob/main/images/algo.png">

## Results
```
Imagenette zero shot classification: 10 classes, subset of Imagenet
Three settings: 
● Prompt ensembling (original)
● Manual selection and ensembling 
● Mapper-assisted selection and ensembling (ours)
```

<img src = "https://github.com/axit54/Prompt-Engineering-for-Vision-Language-Models/blob/main/images/accuracy_map.png">

## Some Other Observations
```
Topologies are similar for synonyms.
```

<img src = "https://github.com/axit54/Prompt-Engineering-for-Vision-Language-Models/blob/main/images/syn_1.png">

<img src = "https://github.com/axit54/Prompt-Engineering-for-Vision-Language-Models/blob/main/images/syn_2.png">







