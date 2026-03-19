students = []

def add_student():
    name = input("Enter Name: ")
    roll = input("Enter Roll Number: ")
    marks = input("Enter Marks: ")
    students.append({"Name": name, "Roll": roll, "Marks": marks})
    print("Student Added Successfully!\n")

def view_students():
    if not students:
        print("No records found.\n")
    else:
        for s in students:
            print(s)
        print()

def delete_student():
    roll = input("Enter Roll Number to delete: ")
    for s in students:
        if s["Roll"] == roll:
            students.remove(s)
            print("Deleted Successfully!\n")
            return
    print("Student Not Found!\n")

while True:
    print("1. Add Student")
    print("2. View Students")
    print("3. Delete Student")
    print("4. Exit")
    
    choice = input("Enter Choice: ")
    
    if choice == '1':
        add_student()
    elif choice == '2':
        view_students()
    elif choice == '3':
        delete_student()
    elif choice == '4':
        break
    else:
        print("Invalid Choice\n")
