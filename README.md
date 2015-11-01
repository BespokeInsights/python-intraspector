# Python Intraspector
[![PyPI version](https://badge.fury.io/py/intraspector.svg)](https://badge.fury.io/py/intraspector)

This project is currently under development. APIs will change.

## Example Usage
Declare Intraspector object
```python
from intraspector import Intraspector
global intraspector
intraspector = Intraspector()
```

Add Intraspector decorator to functions you want recorded.
```python

@intraspector.record()
def somefunction(args, kwargs):
  secondCall(args)

@intraspector.record()
def secondCall(args):
  dont_record_this()

def dont_record_this():
  # Do something
```

Return Intraspector trace
```python
if intraspector.get_debug_mode:
    value['intraspector_trace'] = intraspector.get_trace()
```

## Related Modules
[React Fluxible Intraspector](https://github.com/BespokeInsights/react-fluxible-intraspector)


## Thanks
Proudly developed by [Bespoke Insights](http://BespokeInsights.github.io)
