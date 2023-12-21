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

## Como citar

```
@article{Schneider_Gumiel_Oliveira_Montenegro_Barzotto_Moro_Pagano_Paraiso_2023, place={Brasil}, title={Developing a Transformer-based Clinical Part-of-Speech Tagger for Brazilian Portuguese}, volume={15}, url={https://jhi.sbis.org.br/index.php/jhi-sbis/article/view/1086}, DOI={10.59681/2175-4411.v15.iEspecial.2023.1086}, abstractNote={&amp;lt;p&amp;gt;Electronic Health Records are a valuable source of information to be extracted by means of natural language processing (NLP) tasks, such as morphosyntactic word tagging. Although there have been significant advances in health NLP, such as the Transformer architecture, languages such as Portuguese are still underrepresented. This paper presents taggers developed for Portuguese texts, fine-tuned using BioBERtpt (clinical/biomedical) and BERTimbau (generic) models on a POS-tagged corpus. We achieved an accuracy of 0.9826, state-of-the-art for the corpus used. In addition, we performed a human-based evaluation of the trained models and others in the literature, using authentic clinical narratives. Our clinical model achieved 0.8145 in accuracy compared to 0.7656 for the generic model. It also showed competitive results compared to models trained specifically with clinical texts, evidencing domain impact on the base model in NLP tasks.&amp;lt;/p&amp;gt;}, number={Especial}, journal={Journal of Health Informatics}, author={Schneider, Elisa Terumi Rubel and Gumiel, Yohan Bonescki and Oliveira, Lucas Ferro Antunes de and Montenegro, Carolina de Oliveira and Barzotto, Laura Rubel and Moro, Claudia and Pagano, Adriana and Paraiso, Emerson Cabrera}, year={2023}, month={jul.} }
```
