
# Binary Exponentiation
Binary exponentiation is a technique for calculating the power of a number to a large exponent. It is a recursive algorithm that works by repeatedly squaring the base number and then multiplying the result by the exponent. The algorithm is efficient because it only requires a constant number of multiplications, regardless of the size of the exponent.

To calculate an using binary exponentiation, we first write n in binary. Then, we repeatedly square a and multiply the result by the binary digits of n, starting from the right. For example, to calculate 210, we would write 10 in binary as 1010. Then, we would square 2 twice, getting 4. Then, we would multiply 4 by the first binary digit of n, which is 1, getting 4. Finally, we would multiply 4 by the second binary digit of n, which is 0, getting 4. The result is 210=1024.

Binary exponentiation can be used to calculate the power of a number to any exponent, but it is particularly useful for calculating powers of large numbers. This is because the number of multiplications required by binary exponentiation is proportional to the logarithm of the exponent, rather than the exponent itself. For example, to calculate 21000 using binary exponentiation, we would only need to perform 30 multiplications. This is much faster than the naive algorithm, which would require 1000 multiplications.

Binary exponentiation is a powerful algorithm that has many applications. It is used in cryptography, number theory, and other areas of mathematics. It is also used in some computer algorithms, such as the quicksort algorithm.

 - This is  how it will work in python
 
```
```python
def  binary_exponentiation(a, n):
	if  n == 0:
		return  1
	if  n % 2 == 0:
		return  binary_exponentiation(a, n // 2) ** 2
	else:
		return  a * binary_exponentiation(a, n // 2) ** 2

  

print(binary_exponentiation(2, 10))
```

The code starts by checking if the exponent is 0. If it is, the function returns 1, since any number to the power of 0 is 1.

If the exponent is not 0, the function checks if the exponent is even. If it is, the function calls itself recursively to calculate the power of a to n // 2, and then squares the result. This is because a to the power of n is equal to (a to the power of n // 2) to the power of 2.

If the exponent is odd, the function multiplies a by the result of the recursive call to calculate the power of a to n // 2. This is because a to the power of n is equal to a to the power of n // 2 multiplied by a.
