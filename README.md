# Ex No: 08 - HAMMING - SHANNON_FANO
Consider a discrete memoryless source withsymbols and statistics {0.125, 0.0625, 0.25,0.0625, 0.125, 0.125, 0.25} for its output.Apply the Huffman and Shannon-Fano tothis source.

## Aim

## Tools Required

Python: A versatile language for scientific computing and signal processing.
NumPy & Matplotlib: Libraries for numerical operations and high-quality visualizations,essential for demonstrating sampling.


## Program:
~~~
Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")


~~~
## Output:
![image](https://github.com/user-attachments/assets/5994c86b-0bed-4115-bbc5-e873ce12a6f7)
## Calculation:
![WhatsApp Image 2025-03-30 at 15 47 18_338fc08f](https://github.com/user-attachments/assets/d1679930-50a3-45be-9c83-051e3dd6266f)
![WhatsApp Image 2025-03-30 at 15 47 19_4e7c19a7](https://github.com/user-attachments/assets/0e4075c2-b3e3-4671-a253-997fd596c23b)












## Results:
For the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25.
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0 %
Redudancy is : 0.0
Variance is : 0.484.
