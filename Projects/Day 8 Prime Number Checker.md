# Instructions
Prime numbers are numbers that can only be cleanly divided by themselves and 1.

https://en.wikipedia.org/wiki/Prime_number

You need to write a function that checks whether if the number passed into it is a prime number or not.
```
e.g. 2 is a prime number because it's only divisible by 1 and 2.

But 4 is not a prime number because you can divide it by 1, 2 or 4.
```
### Example Input 1
```
73
```
### Example Output 1
```
It's a prime number.
```
### Example Input 2
```
75
```
### Example Output 2
```
It's not a prime number.
```
```python
def prime_checker(number):
    # Check if the number is greater than 0
    if number > 0:
        count = 0
        # Iterate through numbers from 1 to the given number
        for i in range(1, number+1):
            # Check if the number is divisible by i
            if number % i == 0:
                count += 1
        
        # If the count of divisors is 2, it's a prime number
        if count == 2:
            print("It's a prime number.")
        else:
            print("It's not a prime number.")
    else:
        print("Please enter a positive integer.")

print("Welcome to the Prime Number Checker\n")

# Prompt the user to enter a number and convert it to an integer
n = int(input("Enter a number: "))  # Check this number

# Call the prime_checker function with the input number
prime_checker(number=n)
```
