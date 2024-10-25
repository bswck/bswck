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

#### `education`
`# TODO(bswck#1): fill in this section`

