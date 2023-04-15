# function to calculate numerology number
def calculate_numerology(date_of_birth):
    # convert date of birth to a string and remove all non-digit characters
    dob_str = str(date_of_birth)
    dob_str = "".join(filter(str.isdigit, dob_str))
    
    # calculate the sum of digits in the date of birth
    dob_sum = sum(int(digit) for digit in dob_str)
    
    # if the sum is greater than 9, then sum the digits again to obtain a single-digit number
    if dob_sum > 9:
        dob_sum = sum(int(digit) for digit in str(dob_sum))
    
    return dob_sum

# get user input
name = input("Enter your name: ")
date_of_birth = input("Enter your date of birth (in DD/MM/YYYY format): ")

# calculate numerology number
numerology_number = calculate_numerology(date_of_birth)

# print message
print(f"Hello {name}! Your numerology number is {numerology_number}.")
if numerology_number == 1:
    print("You are a natural born leader and have a strong sense of self.")
elif numerology_number == 2:
    print("You are a sensitive and intuitive person who values harmony and balance.")
elif numerology_number == 3:
    print("You are a creative and expressive person who enjoys socializing and entertaining.")
elif numerology_number == 4:
    print("You are a hardworking and practical person who values stability and security.")
elif numerology_number == 5:
    print("You are a free-spirited and adventurous person who enjoys experiencing new things.")
elif numerology_number == 6:
    print("You are a nurturing and caring person who values family and community.")
elif numerology_number == 7:
    print("You are a thoughtful and introspective person who enjoys solitude and contemplation.")
elif numerology_number == 8:
    print("You are a powerful and ambitious person who values success and achievement.")
elif numerology_number == 9:
    print("You are a compassionate and humanitarian person who values helping others.")
else:
    print("Your numerology number is not recognized.")
