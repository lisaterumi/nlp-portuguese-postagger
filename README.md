# NLP Portuguese POS-tagger

Treinamos o modelo [BERTimbau](https://github.com/neuralmind-ai/portuguese-bert/) com o corpus [MacMorpho](http://nilc.icmc.usp.br/macmorpho/) para tarefa de *POS-Tagger*, com 10 épocas, atingindo um *F1-Score* geral de `0.9826`.

Metricas:

```
              Precision  Recall  F1    Suport
accuracy                         0.98  33729
macro avg     0.96       0.95    0.95  33729
weighted avg  0.98       0.98    0.98  33729

F1:  0.9826  Accuracy:  0.9826
```

## Repositório

Nosso modelo está no repositório oficial do `Hugging Faces`, você pode acessá-lo pelo endereço: https://huggingface.co/lisaterumi/postagger-portuguese/

<img src="postagger_elisa.png">

Se você gostou do nosso trabalho, não se esqueça de dar um *like* no modelo no `Hugging Faces` ❤️

## Como usar

Para usar nosso modelo, basta seguir os passos abaixo:

```
from transformers import AutoTokenizer, AutoModelForTokenClassification

tokenizer = AutoTokenizer.from_pretrained("lisaterumi/postagger-portuguese")

model = AutoModelForTokenClassification.from_pretrained("lisaterumi/postagger-portuguese")

```

Aqui você tem um manual dos tipos gramaticais retornados pelo modelo:

| Sigla  |  Significado  |
| ------------------- | ------------------- |
|  ADJ |  Adjetivo |
|  ADV |  Advérbio |
|  ADV-KS |  Advérbio conjuntivo subordinado  |
|  ADV-KS-REL |   Advérbio relativo subordinado |
|  ART |  Artigo  |
|  CUR |  Moeda  |
|  IN |  Interjeição |
|  KC |  Conjunção coordenativa |
|  KS |  Conjunção subordinativa |
|  N |  Substantivo |
|  NPROP | Substantivo próprio |
|  NUM |  Número |
|  PCP |  Particípio |
|  PDEN |  Palavra denotativa |
|  PREP |  Preposição |
|  PROADJ |  Pronome Adjetivo |
|  PRO-KS |  Pronome conjuntivo subordinado |
|  PRO-KS-REL |  Pronome relativo conectivo subordinado |
|  PROPESS |  Pronome pessoal |
|  PROSUB |  Pronome nominal |
|  V | Verbo |
|  VAUX  | Verbo auxiliar |


Mais informações e exemplos em: http://nilc.icmc.usp.br/macmorpho/macmorpho-manual.pdf
