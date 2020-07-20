# coordinator

A simple library that manages hooks in Python applications.

[![PyPI version](https://badge.fury.io/py/coordinator.svg)](https://badge.fury.io/py/coordinator)

## Install

```sh
pip install coordinator
```

## Example

Simplest example

```py
from gevent import monkey; monkey.patch_all()
from coordinator import Coordinator

coord = Coordinator()

@coord.register_task("my_hook")
def my_task(context):
    print(context["message"])

coord.fire_hook("my_hook", {
    "message": "Hello, World!"
})

```

Full documentation is WIP.
