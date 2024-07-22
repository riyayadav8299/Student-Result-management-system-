# Student-Result-management-system-class Student:
    def __init__(self, roll_no, name, marks):
        self.roll_no = roll_no
        self.name = name
        self.marks = marks

class StudentMarksManagementSystem:
    def __init__(self):
        self.students = []

    def add_student(self, roll_no, name, marks):
        student = Student(roll_no, name, marks)
        self.students.append(student)
        print(f"Student {name} added successfully.")

    def display_students(self):
        if not self.students:
            print("No student records available.")
            return

        for student in self.students:
            print(f"Roll No: {student.roll_no}, Name: {student.name}, Marks: {student.marks}")

    def calculate_average_marks(self):
        if not self.students:
            print("No student records available.")
            return

        total_marks = sum(student.marks for student in self.students)
        average_marks = total_marks / len(self.students)
        print(f"Average Marks: {average_marks:.2f}")

# Example Usage
sms = StudentMarksManagementSystem()
sms.add_student(1, 'Alice', 85)
sms.add_student(2, 'Bob', 90)
sms.add_student(3, 'Charlie', 78)

sms.display_students()
sms.calculate_average_marks()
