# textcat_umberto


## Install


```bash
pip install -r requirements.txt
pip install https://github.com/Gianpe/texcat_umberto/releases/download/v0.0.2/it_textcat_umberto-0.0.2-py3-none-any.whl
```


```{python}
import spacy

text = "che disorganizzazione ad agrigento! sono in quarantena da 7 giorni e non ho ancora ricevuto una chiamata dalla provincia"
nlp = spacy.load("it_textcat_umberto")
demo = nlp(text)
print(demo.cats)
```

## Training

Clone repository and install requirements
```bash
git clone https://github.com/Gianpe/textcat_umberto.git
pip install -r requirements.txt
```

Pass your wandb API key to track the training
```bash
wandb login
```

Run training pipeline
```bash
spacy project run preprocess
spacy project run train
spacy project run evaluate
```

Create python package
```bash
spacy package /content/textcat_goemotions/training/bert/model-best /content/textcat_goemotions/packages/ --name textcat_umberto --force --version 0.0.2 --build wheel
```
