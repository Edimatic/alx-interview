#	0x02. Minimum Operations

To solve this problem, you need to consider that the operations allowed are "Copy All" and "Paste". The key idea is to factorize the number n and use those factors to determine the minimum number of operations required.

##	Here's the plan:

Start with 1 "H".

If n is not 1, repeatedly divide n by the smallest possible divisor (starting from 2) and count the operations needed.

The smallest divisor represents the times you need to "Copy All" and "Paste" to multiply the current number of "H"s.


The minimum operations needed are the sum of these divisors. Here's the implementation:


#	Explanation:

The function minOperations takes an integer n as input.

If n is less than or equal to 1, it's impossible to achieve, so the function returns 0.

The function tries to divide n by the smallest divisor starting from 2. Each time it can divide n by divisor, it adds the divisor to the count of operations and reduces n.

The loop continues until n is reduced to 1.

#	Testing:
Here’s how you can test the function using the provided 0-main.py:
