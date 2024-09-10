def calculate_average(numbers):
    """Calculate the average of a list of numbers."""
    if not numbers:
        return 0
    return sum(numbers) / len(numbers)

def main():
    """Main function to handle user input and calculate the average."""
    print("Welcome to the Average Calculator!")
    print("Enter your numbers separated by spaces.")
    print("Type 'done' when you are finished.")

    while True:
        user_input = input("Enter numbers: ").strip()
        
        if user_input.lower() == 'done':
            break

        try:
            # Convert the input string into a list of floats
            numbers = [float(x) for x in user_input.split()]
            average = calculate_average(numbers)
            print(f"The average is: {average:.2f}")
        except ValueError:
            print("Invalid input. Please enter numbers separated by spaces.")

if __name__ == "__main__":
    main()
