# textcat_umberto


## USAGE


```bash
pip install -r requirements.txt
pip install https://github.com/Gianpe/texcat_umberto/releases/download/v0.0.1/it_textcat_emotion_umberto-0.0.1-py3-none-any.whl
```


```{python}
import spacy

text = "che disorganizzazione ad agrigento! sono in quarantena da 7 giorni e non ho ancora ricevuto una chiamata dalla provincia"
nlp = spacy.load("it_textcat_emotion_umberto")
demo = nlp(text)
print(demo.cats)
```
