# logger
Boilerplate config for logging config

Inspired by  [this blog](https://fangpenlin.com/posts/2012/08/26/good-logging-practice-in-python/)

## Init logger in every module
*__init__.py*
```
import logging
logging.getLogger(__name__).addHandler(logging.NullHandler())
```

*module.py*
```
import logging
def __init__(self)
    self.logger = logging.getLogger('module.ClassName')
```

## Init logger in the top level script
```
import logging.config
logger = logging.getLogger(__name__)
with open('logger/dev.json', 'rt') as f:
    config = json.load(f)
logging.config.dictConfig(config)
```
