### `about`
Mainly programming and teaching Python. Contact me via e-mail, [📧 bartoszpiotrslawecki@gmail.com](mailto://bartoszpiotrslawecki@gmail.com).

My main areas of interest are probably education & metaprogramming.

#### `education`
I'm a technical trainer with a focus on Python, Git and whatever else is on our way.

Feel free to reach out, especially if:
- you are a beginner willing to learn how to think like a programmer
- you are a professional willing to get deep understanding of particular concepts in Python

#### `metaprogramming`
I'm making a library called [injection](https://github.com/bswck/injection):

```py
from functools import partial
from random import randint

from injection import inject

roll: int
inject("roll", into=locals(), factory=partial(randint, 1, 6))

print(roll)  # 6
print(roll)  # 4
print(roll)  # 3

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


