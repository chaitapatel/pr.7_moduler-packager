import sys
import time
import math
import random
import uuid
import string
from datetime import datetime

# Import custom toolkit package
import toolkit.file_ops as file_ops
import toolkit.math_ops as math_ops


# ==================== 1. DATETIME & TIME OPERATIONS ====================
def datetime_operations():
    while True:
        print("\n" + "=" * 30)
        print("Datetime and Time Operations:")
        print("1. Display current date and time")
        print("2. Calculate difference between two dates/times")
        print("3. Format date into custom format")
        print("4. Stopwatch")
        print("5. Countdown Timer")
        print("6. Back to Main Menu")
        choice = input("Enter your choice: ").strip()

        if choice == '1':
            now = datetime.now()
            print(f"\nCurrent Date and Time: {now.strftime('%Y-%m-%d %H:%M:%S')}")
            print("=" * 30)

        elif choice == '2':
            d1_str = input("Enter the first date (YYYY-MM-DD): ").strip()
            d2_str = input("Enter the second date (YYYY-MM-DD): ").strip()
            try:
                d1 = datetime.strptime(d1_str, "%Y-%m-%d")
                d2 = datetime.strptime(d2_str, "%Y-%m-%d")
                diff = abs((d2 - d1).days)
                print(f"Difference: {diff} days")
            except ValueError:
                print("Invalid date format! Use YYYY-MM-DD.")
            print("=" * 30)

        elif choice == '3':
            fmt = input("Enter format (e.g., %d-%m-%Y or %B %d, %Y): ").strip()
            if not fmt:
                fmt = "%d/%m/%Y %I:%M %p"
            print(f"Formatted Date: {datetime.now().strftime(fmt)}")
            print("=" * 30)

        elif choice == '4':
            input("Press Enter to start stopwatch...")
            start_t = time.time()
            input("Press Enter to stop...")
            elapsed = time.time() - start_t
            print(f"Elapsed Time: {elapsed:.2f} seconds")
            print("=" * 30)

        elif choice == '5':
            try:
                sec = int(input("Enter countdown time in seconds: "))
                for remaining in range(sec, 0, -1):
                    print(f"Time left: {remaining}s", end="\r")
                    time.sleep(1)
                print("\nTime's up!")
            except ValueError:
                print("Please enter a valid integer.")
            print("=" * 30)

        elif choice == '6':
            break
        else:
            print("Invalid choice! Try again.")


# ==================== 2. MATHEMATICAL OPERATIONS ====================
def mathematical_operations():
    while True:
        print("\n" + "=" * 30)
        print("Mathematical Operations:")
        print("1. Calculate Factorial")
        print("2. Solve Compound Interest")
        print("3. Trigonometric Calculations")
        print("4. Area of Geometric Shapes")
        print("5. Back to Main Menu")
        choice = input("Enter your choice: ").strip()

        if choice == '1':
            try:
                num = int(input("Enter a number: "))
                print(f"Factorial: {math_ops.factorial(num)}")
            except ValueError as e:
                print(f"Error: {e}")
            print("=" * 30)

        elif choice == '2':
            try:
                p = float(input("Enter principal amount: "))
                r = float(input("Enter rate of interest (in %): "))
                t = float(input("Enter time (in years): "))
                ci = math_ops.compound_interest(p, r, t)
                print(f"Compound Interest: {ci}")
            except ValueError:
                print("Invalid numerical inputs.")
            print("=" * 30)

        elif choice == '3':
            try:
                deg = float(input("Enter angle in degrees: "))
                rad = math.radians(deg)
                print(f"sin({deg}) = {round(math.sin(rad), 4)}")
                print(f"cos({deg}) = {round(math.cos(rad), 4)}")
                print(f"tan({deg}) = {round(math.tan(rad), 4)}")
            except ValueError:
                print("Invalid input.")
            print("=" * 30)

        elif choice == '4':
            print("Shapes: 1. Circle  2. Rectangle  3. Triangle")
            s_opt = input("Select shape: ").strip()
            try:
                if s_opt == '1':
                    r = float(input("Radius: "))
                    print(f"Area: {math_ops.shape_area('circle', r)}")
                elif s_opt == '2':
                    l = float(input("Length: "))
                    w = float(input("Width: "))
                    print(f"Area: {math_ops.shape_area('rectangle', l, w)}")
                elif s_opt == '3':
                    b = float(input("Base: "))
                    h = float(input("Height: "))
                    print(f"Area: {math_ops.shape_area('triangle', b, h)}")
                else:
                    print("Invalid shape choice.")
            except ValueError:
                print("Invalid dimension input.")
            print("=" * 30)

        elif choice == '5':
            break
        else:
            print("Invalid choice! Try again.")


# ==================== 3. RANDOM DATA GENERATION ====================
def random_data_generation():
    while True:
        print("\n" + "=" * 30)
        print("Random Data Generation:")
        print("1. Generate Random Number")
        print("2. Generate Random List")
        print("3. Create Random Password")
        print("4. Generate Random OTP")
        print("5. Back to Main Menu")
        choice = input("Enter your choice: ").strip()

        if choice == '1':
            try:
                start = int(input("Enter minimum range: "))
                end = int(input("Enter maximum range: "))
                print(f"Random Number: {random.randint(start, end)}")
            except ValueError:
                print("Invalid integer inputs.")
            print("=" * 30)

        elif choice == '2':
            try:
                size = int(input("Enter list size: "))
                r_list = [random.randint(1, 100) for _ in range(size)]
                print(f"Random List: {r_list}")
            except ValueError:
                print("Invalid size.")
            print("=" * 30)

        elif choice == '3':
            try:
                length = int(input("Enter password length: "))
                chars = string.ascii_letters + string.digits + "!@#$%^&*()"
                pwd = ''.join(random.choice(chars) for _ in range(length))
                print(f"Generated Password: {pwd}")
            except ValueError:
                print("Invalid length.")
            print("=" * 30)

        elif choice == '4':
            otp = random.randint(100000, 999999)
            print(f"Generated 6-Digit OTP: {otp}")
            print("=" * 30)

        elif choice == '5':
            break
        else:
            print("Invalid choice! Try again.")


# ==================== 4. UUID GENERATION ====================
def uuid_generation():
    print("\n" + "=" * 30)
    print("Generate Unique Identifiers:")
    new_uuid = uuid.uuid4()
    print(f"Generated UUID: {new_uuid}")
    print("=" * 30)


# ==================== 5. CUSTOM FILE OPERATIONS ====================
def file_operations_menu():
    while True:
        print("\n" + "=" * 30)
        print("File Operations:")
        print("1. Create a new file")
        print("2. Write to a file")
        print("3. Read from a file")
        print("4. Append to a file")
        print("5. Back to Main Menu")
        choice = input("Enter your choice: ").strip()

        if choice == '1':
            fn = input("Enter file name: ").strip()
            print(file_ops.create_file(fn))
            print("=" * 30)

        elif choice == '2':
            fn = input("Enter file name: ").strip()
            data = input("Enter data to write: ")
            print(file_ops.write_to_file(fn, data))
            print("=" * 30)

        elif choice == '3':
            fn = input("Enter file name: ").strip()
            print("File Content:")
            print(file_ops.read_file(fn))
            print("=" * 30)

        elif choice == '4':
            fn = input("Enter file name: ").strip()
            data = input("Enter data to append: ")
            print(file_ops.append_to_file(fn, data))
            print("=" * 30)

        elif choice == '5':
            break
        else:
            print("Invalid choice! Try again.")


# ==================== 6. DYNAMIC MODULE EXPLORATION ====================
def explore_module_attributes():
    print("\n" + "=" * 30)
    print("Explore Module Attributes:")
    mod_name = input("Enter module name to explore (e.g., math, random, time): ").strip()
    try:
        module = sys.modules.get(mod_name) or __import__(mod_name)
        attrs = [attr for attr in dir(module) if not attr.startswith("__")]
        print(f"Available Attributes in {mod_name} module:")
        print(attrs[:15], "...")  # Preview first 15 attributes
    except ImportError:
        print(f"Module '{mod_name}' not found or cannot be imported.")
    print("=" * 30)


# ==================== MAIN EXECUTION LOOP ====================
def main():
    while True:
        print("\n" + "=" * 30)
        print("Welcome to Multi-Utility Toolkit")
        print("=" * 30)
        print("Choose an option:")
        print("1. Datetime and Time Operations")
        print("2. Mathematical Operations")
        print("3. Random Data Generation")
        print("4. Generate Unique Identifiers (UUID)")
        print("5. File Operations (Custom Module)")
        print("6. Explore Module Attributes (dir())")
        print("7. Exit")
        print("=" * 30)

        choice = input("Enter your choice: ").strip()

        if choice == '1':
            datetime_operations()
        elif choice == '2':
            mathematical_operations()
        elif choice == '3':
            random_data_generation()
        elif choice == '4':
            uuid_generation()
        elif choice == '5':
            file_operations_menu()
        elif choice == '6':
            explore_module_attributes()
        elif choice == '7':
            print("\n" + "=" * 30)
            print("Thank you for using the Multi-Utility Toolkit!")
            print("=" * 30)
            break
        else:
            print("Invalid choice. Please choose between 1 and 7.")

if __name__ == "__main__":
    main()