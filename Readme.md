# NLP - BILSTM Named Entity Recognition

# Architecture

<center><img src="model.png"></center>

# Libraries

```yaml
tensorflow
keras
keras-contrib
sklearn-crfsuite
seqeval
numpy
pandas
```

# [Dataset](input/ner_dataset.csv)

| Sentence #  | Word        | POS | Tag     |
| ----------- | ----------- | --- | ------- |
| Sentence: 0 | studies     | NNS | O       |
| Sentence: 0 | on          | IN  | O       |
| Sentence: 0 | magnesium   | NN  | O       |
| Sentence: 0 | s           | NN  | O       |
| Sentence: 0 | mechanism   | NN  | O       |
| Sentence: 0 | of          | IN  | O       |
| Sentence: 0 | action      | NN  | O       |
| Sentence: 0 | in          | IN  | O       |
| Sentence: 0 | digitalis   | NN  | plant   |
| Sentence: 0 | induced     | VBD | O       |
| Sentence: 0 | arrhythmias | NNS | disease |
...

# Config

```yaml
validation_split =0.2,
batch_size = 32,
epochs = 3,
verbose =1
```

# Scores

```
Loss        : 0.09244067221879959
Precision   : 0.9714112281799316
Recall      : 0.9714112281799316
Accuracy    : 0.9688527584075928
F-1 Score   : 0.9714111089706421
```
# Model Summary

```yaml
Model: "model"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 input_1 (InputLayer)        [(None, 137)]             0         
                                                                 
 embedding (Embedding)       (None, 137, 137)          423330    
                                                                 
 dropout (Dropout)           (None, 137, 137)          0         
                                                                 
 bidirectional (Bidirectiona  (None, 137, 200)         190400    
 l)                                                              
                                                                 
 time_distributed (TimeDistr  (None, 137, 3)           603       
 ibuted)                                                         
                                                                 
=================================================================
Total params: 614,333
Trainable params: 614,333
Non-trainable params: 0
_________________________________________________________________
```

# Model Output

```yaml
-drwxrwxrwx 1 dimas dimas 4.0K Jun 26 23:09 assets
-rwxrwxrwx 1 dimas dimas  19K Jun 25 17:24 keras_metadata.pb
-rwxrwxrwx 1 dimas dimas 1.5M Jun 25 17:24 saved_model.pb
-rwxrwxrwx 1 dimas dimas 7.1M Jun 25 17:24 variables.data-00000-of-00001        
-rwxrwxrwx 1 dimas dimas 2.7K Jun 25 17:24 variables.index
```