# [Failed loading english.pickle with nltk.data.load](https://stackoverflow.com/questions/4867197/failed-loading-english-pickle-with-nltk-data-load)
> [!error] When trying to load the `punkt` tokenizer...
> ```python
> import nltk.data
> tokenizer = nltk.data.load('nltk:tokenizers/punkt/english.pickle')
> ```
> 
> ...a `LookupError` was raised:
> 
```python
> LookupError: 
>     *********************************************************************   
> Resource 'tokenizers/punkt/english.pickle' not found.  Please use the NLTK Downloader to obtain the resource: nltk.download().   Searched in:
>         - 'C:\\Users\\Martinos/nltk_data'
>         - 'C:\\nltk_data'
>         - 'D:\\nltk_data'
>         - 'E:\\nltk_data'
>         - 'E:\\Python26\\nltk_data'
>         - 'E:\\Python26\\lib\\nltk_data'
>         - 'C:\\Users\\Martinos\\AppData\\Roaming\\nltk_data'
>     **********************************************************************
```

> [!tips] Answer

Reference:
[https://www.nltk.org/howto/data.html](https://www.nltk.org/howto/data.html)

I had this same problem. Go into a python shell and type:

```python
>>> import nltk
>>> nltk.download()
```

Then an installation window appears. Go to the 'Models' tab and select 'punkt' from under the 'Identifier' column. Then click Download and it will install the necessary files. Then it should work!