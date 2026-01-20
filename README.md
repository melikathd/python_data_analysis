# python_data_analysis
This project is a simple Python script that works with two types of data: - a list of names - a list of numbers The program filters and analyzes the data, then returns the longest name
def analyz_data(names, numbers):
    filtered_numbers = []
    long_names = []
    longest_name = ""
    for name in names:
        name = name.strip()
        if len(name) > 5:
            long_names.append(name)
            if len(name) > len(longest_name):
                longest_name = name
    for number in numbers:
        if number % 2 != 0 and number > 12:
            filtered_numbers.append(number)
    print("odd numbers greater than 12:", filtered_numbers)
    print("names longer than 5 letters:", long_names)
    return longest_name


names = ["Maryam", "lila", "mohammadreza", "lilin"]
numbers = [13, 15, 4, 5, 25, 21]
result = analyz_data(names, numbers)
print("the longest name is :", result)
