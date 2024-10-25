### `about`
Mainly programming and teaching Python. Contact me [📧 bartoszpiotrslawecki@gmail.com](mailto://bartoszpiotrslawecki@gmail.com).

My main areas of interest are probably metaprogramming & education.

#### `metaprogramming`
I'm making a library called [injection](https://github.com/bswck/injection):

```py
from functools import partial
from random import randint

from injection import injection

roll: int
injection("roll", factory=partial(randint, 1, 6), into=locals())

print(roll)  # 6
print(roll)  # 4
print(roll)  # 3
```

```py
from __future__ import annotations

from injection.contrib import lazy_imports, type_imports

with type_imports():
    from _typeshed import StrPath  # never imported, typing.Any at runtime

with lazy_imports():
    import pandas as pd

def read_data(path: StrPath) -> pd.DataFrame:
    return pd.read_csv(path, sep=";")  # pandas only imported now
```

#### `education`
`# TODO(bswck#1): fill in this section`

