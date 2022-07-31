# NLP
# Named Entity Recognition (NER) - BILSTM


## <img src="https://img.icons8.com/external-smashingstocks-flat-smashing-stocks/64/000000/external-manager-hotel-smashingstocks-flat-smashing-stocks-2.png"/> **`Slamet Riyanto S.Kom., M.M.S.I.`**

## <img src="https://img.icons8.com/external-fauzidea-flat-fauzidea/64/undefined/external-man-avatar-avatar-fauzidea-flat-fauzidea.png"/> **`Dimas Dwi Putra`**

## Architecture
<img src="NER-BILSTM%20Architecture.png" WIDTH="2343">

## Dataset
| Sentence #  | Word        | POS | Tag       |
| ----------- | ----------- | --- | --------- |
| Sentence: 0 | studies     | NNS | O         |
| Sentence: 0 | on          | IN  | O         |
| Sentence: 0 | magnesium   | NN  | O         |
| Sentence: 0 | s           | NN  | O         |
| Sentence: 0 | mechanism   | NN  | O         |
| Sentence: 0 | of          | IN  | O         |
| Sentence: 0 | action      | NN  | O         |
| Sentence: 0 | in          | IN  | O         |
| Sentence: 0 | digitalis   | NN  | B-plant   |
| Sentence: 0 | induced     | VBD | O         |
| Sentence: 0 | arrhythmias | NNS | B-disease |
...

## Eval
| Entities     | precision | recall   | f1-score | support | excecution time | processor | ram  | model | batch size | epochs |
| ------------ | --------- | -------- | -------- | ------- | --------------- | --------- | ---- | ----- | ---------- | ------ |
| PAD          | 0,976923  | 0,976923 | 0,976923 | 130     | 0.06.21         | CPU       | High | 1     | 16         | 20     |
| Disease      | 0,460432  | 0,450704 | 0,455516 | 142     |                 |           |      |       |            |        |
| Plant        | 0,854962  | 0,829630 | 0,842105 | 135     |                 |           |      |       |            |        |
| micro avg    | 0,757500  | 0,744472 | 0,750929 | 407     |                 |           |      |       |            |        |
| macro avg    | 0,764106  | 0,752419 | 0,758181 | 407     |                 |           |      |       |            |        |
| weighted avg | 0,756268  | 0,744472 | 0,750289 | 407     |                 |           |      |       |            |        |
| F-1 Scores   |           |          | 75,10%   |         |                 |           |      |       |            |        |

## Predict
```yaml
Sample number 2 of 131 (Test Set)
Word           ||True ||Pred
==============================
background     : O     O
and            : O     O
aims           : O     O
large          : O     O
scale          : O     O
epidemiological: O     O
studies        : O     O
have           : O     O
shown          : O     O
that           : O     O
drinking       : O     O
more           : O     O
than           : O     O
two            : O     O
cups           : O     O
of             : O     O
coffee         : plant plant
per            : O     O
day            : O     O
reduces        : O     O
the            : O     O
risks          : O     O
hepatitis      : disease disease
liver          : O     disease
```
## Output
### Save output model as [.hdf5](output/)

# **Other Content**

### **Websites Prediction**
#### [1. Django Websites Prediction For NER dan RE](https://github.com/Dimas263/Django-Websites_NER_RE)


### **Named Entity Recognition (NER)**
#### [1. NER Dataset Biomedical Plant-Disease Corpus](https://github.com/Dimas263/NLP_NER_Dataset_Biomedical_Plant-Disease_Corpus)
#### [2. NER CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_CRF_Named_Entity_Recognition)
#### [3. NER BiLSTM Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BILSTM_Named_Entity_Recognition)
#### [4. NER BERT Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BERT_Named_Entity_Recognition)
#### [5. NER BiLSTM CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BILSTM_CRF_Named_Entity_Recognition)
#### [6. NER BERT BiLSTM CRF Named Entity Recognition](https://github.com/Dimas263/NLP_NER_BERT_BILSTM_CRF_Named_Entity_Recognition)


### **Relation Extraction (NER)**
#### [1. RE Dataset Biomedical Plant-Disease Corpus](https://github.com/Dimas263/NLP_RE_Dataset_Biomedical_Plant-Disease_Corpus)
#### [2. RE BERT Relation Extraction Biomedical](https://github.com/Dimas263/NLP_RE_BERT_Relation_Extraction_Biomedical)
#### [3. RE BiLSTM CRF Relation Extraction Biomedical](https://github.com/Dimas263/NLP_RE_BILSTM_CRF_Relation_Extraction_Biomedical)
