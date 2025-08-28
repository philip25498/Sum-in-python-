# Sum-in-python-# Task 1: Sum of Integers
def calculate_sum():
    """
    Accepts user input for a list of integers and calculates their sum.
    """
    try:
        # Prompt user for input and split the string into a list of number strings
        user_input = input("Enter a list of integers, separated by spaces: ")
        
        # Use a list comprehension to convert each number string to an integer
        # This handles cases where the input is valid numbers.
        integer_list = [int(num) for num in user_input.split()]
        
        # Calculate the sum of all integers in the list using the built-in sum() function
        total_sum = sum(integer_list)
        
        # Print the original list and the calculated sum
        print(f"The list you entered is: {integer_list}")
        print(f"The sum of all integers in the list is: {total_sum}")

    except ValueError:
        # This block will execute if the user enters non-integer values
        print("Invalid input. Please ensure you only enter integers separated by spaces.")

# Call the function to run the program
calculate_sum()
