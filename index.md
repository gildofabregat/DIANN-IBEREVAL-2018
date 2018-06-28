## DIANN Task - Disability annotation on documents from the biomedical domain


>"Disabilities is an umbrella term, covering impairments, activity limitations, and participation restrictions. An impairment is a problem in body function or structure; an activity limitation is a difficulty encountered by an individual in executing a task or action; while a participation restriction is a problem experienced by an individual in involvement in life situations."
>―― World Health Organization

The main goal of DIANN task is the annotation of disabilities. These conditions affect to a large part of population. For example, they are present in many rare disease. Therefore, it is extremely important to collect information related to them.
There are some tools for the annotation of medical concepts, especially in English, such as Metamap. However, they do not consider disabilities as a distinctive concept, but as any other sign. Thus, they do not allow to distinguish a disability, usually a permanent condition, from other signs associated to diseases.

The corpus provided include annotations of disabilities and annotations of negations when it affects to one or more disabilities.

### Dataset

The dataset has been collected between 2017 and 2018. DIANN's corpus consists of a collection of 500 abstracts from Elsevier journal papers related to the biomedical domain. We have selected those abstracts for which there are available both, the Spanish and the English versions.

#### Format 
This dataset contains annotations about the disabilities appearing in these abstracts using the XML tag <dis>. Disabilities are usually expressed either with a specific word, such as "blindness", or as the limitation or lack of a human function, such as "lack of vision". 

###### English
```xml
Fragile-X syndrome is an inherited form of <dis>mental retardation</dis> with a connective tissue component involving mitral valve prolapse.
```  
```xml
Age related macular degeneration (AMD) is the leading cause of <dis>blindness</dis> in individuals older than 65 years of age.
```  

###### Spanish
```xml
El síndrome X frágil es una forma hereditaria de <dis>retraso mental</dis> con una afectación de tejido conectivo que produce prolapso de la válvula mitral.
```  
```xml
La degeneración macular asociada a la edad (DMAE) constituye la causa principal de <dis>ceguera</dis> en personas mayores de 65 años.
```  

We have annotated the disabilities appearing in these abstracts using the XML tag <dis>. Disabilities are usually expressed either with a specific word, such as "blindness", or as the limitation or lack of a human function, such as "lack of vision". 
  
###### English
```xml
Sight: One month later, she presented with complaints of systemic oedema and <dis>loss of vision </dis>.
```
###### Spanish
```xml
Movilidad: Fampridina-LP a dosis de 10mg cada 12 h es actualmente el único fármaco autorizado para mejorar el <dis>trastorno de la marcha </dis> en adultos con EM.
```  
  
Acronyms referring to a disability have been also annotated with the <dis> tag, but only if the extended version has also appeared in the same abstract. 
  
###### English
```xml
To establish the validity and reliability of the Montreal Cognitive Assessment in Spanish (MoCA-S) to identify <dis>mild cognitive impairment</dis> (<dis>MCI</dis>)... 
```
###### Spanish
```xml
Establecer la validez y confiabilidad del Montreal Evaluación Cognitiva en Español (MoCA-E) para identificar <dis>deterioro cognitivo leve</dis> (<dis>DCL</dis>)...
```
  
It is necessary to take into consideration that disabilities that appear isolated in texts without any context (e. g., search queries) or disabilities that appear in names of associations or entities (e. g., Care Unit for Dementia Patients) have not been annotated. 

```xml
A search strategy in _PubMed_ was designed using the following keywords: (gene OR genomics OR GWAS OR high throughput) AND (hearing loss OR chronic otitis media OR age-related hearing loss OR otosclerosis OR Meniere's disease) during the last 5 years.
```
```xml
... in VLBW infants included in the Universal Hearing Loss Screening Programme at the University Mother-Child Hospital of Gran Canaria (Spain) in the 2007–2010 period.
```

Negation is annotated when it affects one or more disabilities. We have adopted the criteria from the Bioscope corpus for annotating negation in English. For Spanish we have annotated the scope corresponding to the English annotation. Negation is annotated with the <scp> tag. For the sake of clarity, the negation triggers has also been annoted with the <neg> tag. 
  
###### English
```xml
In the patients <scp><neg>without</neg> <dis>dementia</dis></scp>, significant differences were obtained in terms of functional and cognitive status (Barthel index of 52.34±38 and Pfeiffer test with an average score of 1.48 ±3.2 (P<.001)).   
```
###### Spanish
```xml
En pacientes <scp> <neg>sin</neg> <dis>demencia</dis></scp>, se obtienen diferencias significativas en cuanto a la situación funcional y cognitiva (índice de Barthel de 52,34±38 y test de Pfeiffer con una puntuación media de 1,48±3,2 (p<0,001)).
```
You can use the [editor on GitHub](https://github.com/gildofabregat/DIANN-IBEREVAL-2018/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.


#### Statistics

###### English

| English data | Docs | Sents | Tokens | Disabilities | Negations | Negated disabilities |
|--------------|------|-------|--------|--------------|-----------|----------------------|
| Training     | 400  | 4782  | 70919  | 1413         | 40        | 42                   |
| Test         | 100  | 1309  | 18406  | 243          | 23        | 24                   |

###### Spanish

| Spanish data | Docs | Sents | Tokens | Disabilities | Negations | Negated disabilities |
|--------------|------|-------|--------|--------------|-----------|----------------------|
| Training     | 400  | 4639  | 78381  | 1326         | 40        | 41                   |
| Test         | 100  | 1284  | 20567  | 229          | 22        | 23                   |



