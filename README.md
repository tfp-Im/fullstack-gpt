# fullstack-gpt
it just study

## requirements
* python 3.11.4
* pyenv

## start

### if you dont have /env .
```sh
python -m venv ./env
```

### activate envirements .
```sh
source env/bin/activate
```

### deactivate envirements .
```sh
deactivate 
```

### package install
```sh
pip install -r requirements.txt 
```

### comfirm .env
```sh
cp .env.sample .env
# OPENAI_API_KEY=<you shoud open api key>
```


### run streamlit
```sh
streamlit run home.py
```



### etc

#### error
AttributeError: partially initialized module 'nltk' has no attribute 'data' (most likely due to a circular import)

run from python command line
```python
import nltk
import ssl

try:
    _create_unverified_https_context = ssl._create_unverified_context
except AttributeError:
    pass
else:
    ssl._create_default_https_context = _create_unverified_https_context

nltk.download()
```



