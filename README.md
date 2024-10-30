### `about`
I'm a software developer and programming teacher.

#### `education`
As a technical trainer I mainly focus on Python and Git, but am happy to explain whatever else is in the way.

Feel free to reach me out via e-mail ([bartoszpiotrslawecki@gmail.com](mailto://bartoszpiotrslawecki@gmail.com)) especially if:
- you are a beginner willing to learn how to think like a programmer
- you are a professional willing to get deep understanding of particular concepts in Python

I conduct lessons in English and Polish, as preferred.

#### `metaprogramming`
I'm making a library called [injection](https://github.com/bswck/injection):

```py
from functools import partial
from random import randint

from injection import inject

roll: int
inject("roll", into=locals(), factory=partial(randint, 1, 6))

print(roll, type(roll))  # 6 <class 'int'>
print(roll, type(roll))  # 4 <class 'int'>
print(roll, type(roll))  # 3 <class 'int'>

# you never know what the value of roll will be!
```

```py
from __future__ import annotations

from injection.contrib import lazy_imports, type_imports

with lazy_imports():
    import pandas as pd

with type_imports():
    from _typeshed import StrPath  # never imported, typing.Any at runtime

def read_data(path: StrPath) -> pd.DataFrame:
    return pd.read_csv(path, sep=";")  # pandas only imported now
```


