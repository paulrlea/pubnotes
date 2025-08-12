Question 1 : 
```
for i in {1..20}; do mkdir -p a$i/{b1,b2,b3,b4,b5,b6,b7,b8,b9,b10}; done
```
Question 2:
```
 gawk -F '[/:]'  '{sub(/F/, "" $10);print$3, $6}' temps.dat >> out.dat
 ```
![[Pasted image 20240607233759.png]]

Question 3:
![[Pasted image 20240607234324.png]]

Question 4:
![[Pasted image 20240607234950.png]]

```
import matplotlib.pyplot as plt

import numpy as np

  

x = np.linspace(-2, 2, 100)

y = np.exp(-x)

plt.figure(figsize=(8, 6))

plt.plot(x, y)

plt.yscale("log")

plt.show()
```



Question 5:
```
arr = np.arange(1, 100, 2).reshape(10, 5)
```

Question 6:
```
import matplotlib.pyplot as plt

import numpy as np

N = 10

main_diag = np.diag([-2.0] * N)

upper = np.diag([1.0] * (N - 1), k=1)

lower = np.diag([1.0] * (N - 1), k=-1)

matrix = main_diag + upper + lower

```
![[Pasted image 20240607235802.png]]