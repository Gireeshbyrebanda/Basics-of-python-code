# Basics-of-python-code
codes for basics of python
#### Prime Numbers
def is_prime(number):
    if number <= 1:
        return False
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return False
    return True
# Test the function
num = 17
if is_prime(num):
    print(f"{num} is a prime number.")
else:
    print(f"{num} is not a prime number.")

 #### Product of Random Numbers
  # Program to generate a random number between 0 and 5

# importing the random module
import random

print(random.randint(0,5))
#### Squares of Even/Odd Numbers
def main():
    print("Squares of even numbers within the range of 100 to 200:")
    for num in range(100, 201):
        if num % 2 == 0:  # Choosing even numbers
            print(f"{num} squared is {num**2}")

if __name__ == "__main__":
    main()
  #### Word Counter
  def count_words(text):
    words = text.split()
    word_count = {}

    for word in words:
        # Removing punctuation marks like period, comma, etc.
        word = word.strip(".,!?:;'\"")

        # Converting word to lowercase to handle case-insensitive counts
        word = word.lower()

        if word in word_count:
            word_count[word] += 1
        else:
            word_count[word] = 1

    return word_count

def main():
    input_text = "This is a sample text. This text will be used to demonstrate the word counter."
    word_count = count_words(input_text)

    print("Word count:")
    for word, count in word_count.items():
        print(f"'{word}': {count}")

if __name__ == "__main__":
    main()
#### Check For Palindrome
def is_palindrome(s):
    # Removing spaces and punctuation and converting to lowercase
    clean_s = ''.join(char.lower() for char in s if char.isalnum())

    # Checking if the cleaned string is equal to its reverse
    return clean_s == clean_s[::-1]

# Example usage:
input_string = "racecar"
print(is_palindrome(input_string))  # Output: T
