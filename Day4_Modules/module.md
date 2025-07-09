# Tóm tắt Lý thuyết và Ví dụ Code - Ngày 12: Modules

## 1. Module là gì?
- **Module** là một file chứa tập hợp các đoạn mã hoặc hàm có thể được sử dụng lại trong ứng dụng Python khác.
- Một module có thể chỉ chứa một biến, một hàm hoặc một mã nguồn lớn. Cung cấp các chức năng cụ thể.

## 2. Tạo một Module
- Viết mã Python trong một file `.py`. Ví dụ:
```py
# mymodule.py
def generate_full_name(firstname, lastname):
    return firstname + ' ' + lastname
```

## 3. Import một Module
- Dùng từ khóa `import` và tên file (không có đuôi `.py`):
```py
import mymodule
print(mymodule.generate_full_name('Asabeneh', 'Yetayeh'))
```

## 4. Import hàm từ Module
- Có thể import các hàm cụ thể từ module:
```py
from mymodule import generate_full_name, sum_two_nums, person, gravity
print(generate_full_name('Asabneh','Yetayeh'))
print(sum_two_nums(1,9))
mass = 100;
weight = mass * gravity
print(weight)
print(person['firstname'])
```

## 5. Import hàm và đổi tên
- Có thể đổi tên hàm khi import:
```py
from mymodule import generate_full_name as fullname, sum_two_nums as total, person as p, gravity as g
print(fullname('Asabneh','Yetayeh'))
print(total(1, 9))
mass = 100;
weight = mass * g
print(weight)
print(p)
print(p['firstname'])
```

## 6. Import các Module dựng sẵn

### OS Module
- Thực hiện các thao tác với hệ điều hành như tạo thư mục, đổi thư mục, lấy thư mục hiện tại, xóa thư mục:
```py
import os
os.mkdir('directory_name')
os.chdir('path')
os.getcwd()
os.rmdir()
```

### Sys Module
- Quản lý môi trường thực thi Python, lấy tham số dòng lệnh, thoát chương trình, kiểm tra phiên bản, v.v.
```py
import sys
#print(sys.argv[0], argv[1],sys.argv[2])
print('Welcome {}. Enjoy  {} challenge!'.format(sys.argv[1], sys.argv[2]))
# python script.py Asabeneh 30DaysOfPython
# Kết quả: Welcome Asabeneh. Enjoy  30DayOfPython challenge!
sys.exit()
sys.maxsize
sys.path
sys.version
```

### Statistics Module
- Cung cấp các hàm thống kê như mean, median, mode, stdev:
```py
from statistics import *
ages = [20, 20, 4, 24, 25, 22, 26, 20, 23, 22, 26]
print(mean(ages))       # ~22.9
print(median(ages))     # 23
print(mode(ages))       # 20
print(stdev(ages))      # ~2.3
```

### Math Module
- Thực hiện các phép toán toán học và sử dụng hằng số toán học:
```py
import math
print(math.pi)           # 3.141592653589793
print(math.sqrt(2))      # 1.4142135623730951
print(math.pow(2, 3))    # 8.0
print(math.floor(9.81))  # 9
print(math.ceil(9.81))   # 10
print(math.log10(100))   # 2
```
- Import nhiều hàm cùng lúc hoặc tất cả hàm:
```py
from math import pi, sqrt, pow, floor, ceil, log10
print(pi)
print(sqrt(2))
print(pow(2, 3))
print(floor(9.81))
print(ceil(9.81))

from math import *
print(pi)
print(sqrt(2))
```
- Đổi tên hàm khi import:
```py
from math import pi as PI
print(PI)
```

### String Module
- Làm việc với các ký tự, số, ký tự đặc biệt:
```py
import string
print(string.ascii_letters) # abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
print(string.digits)        # 0123456789
print(string.punctuation)   # !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
```

### Random Module
- Sinh số ngẫu nhiên:
```py
from random import random, randint
print(random())   # số thực trong khoảng [0, 1)
print(randint(5, 20)) # số nguyên ngẫu nhiên từ 5 đến 20
```

---

**Tóm lại:**  
- Module giúp tái sử dụng code và tổ chức chương trình tốt hơn.  
- Có thể tự tạo module hoặc sử dụng các module dựng sẵn của Python như os, sys, statistics, math, string, random.  
- Việc import module hoặc hàm có thể linh hoạt, đổi tên theo nhu cầu sử dụng.