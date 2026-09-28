def calculate_average(a1, a2, a3):
    total = a1 + a2 + a3
    avg = total / 3
    return avg


while True:
    num_students = int(input("How many students will be processed? "))

    if num_students >= 3:
        break
    else:
        print("Please enter 3 or more students.\n")


for i in range(num_students):
    print(f"\n--- Student {i + 1} ---")

    name = input("Enter name: ")
    act1 = float(input("Activity 1: "))
    act2 = float(input("Activity 2: "))
    act3 = float(input("Activity 3: "))

    average = calculate_average(act1, act2, act3)

    if 90 <= average <= 100:
        status = "Excellent"
    elif 80 <= average < 90:
        status = "Very Good"
    elif 75 <= average < 80:
        status = "Passed"
    else:
        status = "Failed"

    print("\n--- Result ---")
    print(f"Name: {name}")
    print(f"Activity 1: {act1}")
    print(f"Activity 2: {act2}")
    print(f"Activity 3: {act3}")
    print(f"Average: {round(average, 2)}")
    print(f"Status: {status}")
    print("-" * 25)
