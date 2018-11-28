# **Lesser Known Python Libraries for Data Science**
### Summary of the article writen by [Parul Pandley](https://medium.com/analytics-vidhya/python-libraries-for-data-science-other-than-pandas-and-numpy-95da30568fad?mkt_tok=eyJpIjoiWkdVek1qUXdPRGhqT0RNeSIsInQiOiI1cER4NVI1bXVsWnlVUTNnTkdzSXcyb3pRMk1KQVdvamlFMUhDTzBcL240SUdFdmRsRWt6emxCVVpScGZvbHl3SzAxOFdGV0MxNmJPNmJIVTRra0JISWJqT1ZSekd5RkZSQjNQRTY3VzA5Nmx3a2N3Y0pmdTdQRXVvNW5NSExyMmwifQ%3D%3D)
[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

I've only included libraries I indend to use within the next month or so.

### Wget
Install
``` python
pip install wget
```
Example:
``` python
import wget
url = 'http://www.futurecrew.com/skaven/song_files/mp3/razorback.mp3'
filename = wget.download(url)
100% [................................................] 3841532 / 3841532
filename
'razorback.mp3'
``` 
### Pendulum
Install
``` python
pip install pendulum
```
Example:
``` python
import pendulum
dt_toronto = pendulum.datetime(2012, 1, 1, tz='America/Toronto')
dt_vancouver = pendulum.datetime(2012, 1, 1, tz='America/Vancouver')
print(dt_vancouver.diff(dt_toronto).in_hours())
3
``` 
### FlashText
Install
``` python
pip install flashtext
```
Extract Keywords:
``` python
from flashtext import KeywordProcessor
keyword_processor = KeywordProcessor()
# keyword_processor.add_keyword(<unclean name>, <standardised name>)
keyword_processor.add_keyword('Big Apple', 'New York')
keyword_processor.add_keyword('Bay Area')
keywords_found = keyword_processor.extract_keywords('I love Big Apple and Bay Area.')
keywords_found
['New York', 'Bay Area']
``` 
Replace Keywords:
``` python
keyword_processor.add_keyword('New Delhi', 'NCR region')
new_sentence = keyword_processor.replace_keywords('I love Big Apple and new delhi.')
new_sentence
'I love New York and NCR region.'
``` 

### Dash
Install:
```python
pip install dash==0.29.0  # The core dash backend
pip install dash-html-components==0.13.2  # HTML components
pip install dash-core-components==0.36.0  # Supercharged components
pip install dash-table==3.1.3  # Interactive DataTable component (new!)
```
