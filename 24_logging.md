## Logging


```python
import logging

LOGGER = logging.getLogger(__name__)
format_string = '%(levelname)s: %(asctime)s: %(message)s'
logging.basicConfig(level = logging.ERROR, format = format_string)

```


```python
LOGGER.info('Info level log')
LOGGER.warning('Info warning log')
LOGGER.debug('Info debug log')
LOGGER.error('Info error log')
```

    INFO: 2018-07-13 14:32:22,954: Info level log
    WARNING: 2018-07-13 14:32:22,956: Info warning log
    DEBUG: 2018-07-13 14:32:22,957: Info debug log
    ERROR: 2018-07-13 14:32:22,958: Info error log
    
