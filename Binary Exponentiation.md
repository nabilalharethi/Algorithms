
# Binary Exponentiation
Binary exponentiation is a technique for calculating the power of a number to a large exponent. It is a recursive algorithm that works by repeatedly squaring the base number and then multiplying the result by the exponent. The algorithm is efficient because it only requires a constant number of multiplications, regardless of the size of the exponent.

To understand how the algorithm works, let's consider an example. Suppose we want to calculate 2^10 using binary exponentiation. We would first write 10 in binary as 1010. Then, we would repeatedly square 2 and multiply the result by the binary digits of n, starting from the right.

The first binary digit of n is 1, so we would square 2 and multiply the result by 1. This gives us 4.

The next binary digit of n is 0, so we would square 4 and multiply the result by 0. This gives us 16.

The final result is 4×16=64. This is because 2^10=(2^5)2=322=64.

As you can see, the binary exponentiation algorithm is very efficient. It only requires a constant number of multiplications, regardless of the size of the exponent. This makes it much faster than the naive algorithm for calculating powers of large numbers.


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
