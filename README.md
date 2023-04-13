# DBA-Application

# Question 1

arr = [5, 1, 4, 6, 7, 3, 5, 7, 3]

element_counts = {}

for element in arr:
    if element in element_counts:
        element_counts[element] += 1
    else:
        element_counts[element] = 1

print("Duplicate elements in the array are:")
for element, count in element_counts.items():
    if count > 1:
        print(element)

# Question 2

rows = 6

for i in range(1, rows+1):
    for o in range(i):
        print(i ,end='')
    print()


# Question 3

def calculate_percentage(count, total):
    if total == 0:
        return 0
    else:
        return (count / total) * 100

num_newly_hired_male = int(input("Enter number of newly hired male employees: "))
num_newly_hired_female = int(input("Enter number of newly hired female employees: "))
num_permanent_male = int(input("Enter number of male employees in permanent position: "))
num_permanent_female = int(input("Enter number of female employees in permanent position: "))
num_resigned_male = int(input("Enter number of male employees who resigned: "))
num_resigned_female = int(input("Enter number of female employees who resigned: "))

total_newly_hired = num_newly_hired_male + num_newly_hired_female
total_permanent = num_permanent_male + num_permanent_female
total_resigned = num_resigned_male + num_resigned_female
percent_newly_hired_male = calculate_percentage(num_newly_hired_male, total_newly_hired)
percent_newly_hired_female = calculate_percentage(num_newly_hired_female, total_newly_hired)
percent_permanent_male = calculate_percentage(num_permanent_male, total_permanent)
percent_permanent_female = calculate_percentage(num_permanent_female, total_permanent)
percent_resigned_male = calculate_percentage(num_resigned_male, total_resigned)
percent_resigned_female = calculate_percentage(num_resigned_female, total_resigned)

print("Total number of newly hired employees:", total_newly_hired)
print("Total number of permanent employees:", total_permanent)
print("Total number of resigned employees:", total_resigned)
print("Percentage of newly hired male employees:", percent_newly_hired_male)
print("Percentage of newly hired female employees:", percent_newly_hired_female)
print("Percentage of male employees in permanent position:", percent_permanent_male)
print("Percentage of female employees in permanent position:", percent_permanent_female)
print("Percentage of male employees who resigned:", percent_resigned_male)
print("Percentage of female employees who resigned:", percent_resigned_female)
