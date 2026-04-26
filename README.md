# Student_marks
students = []

def get_grade(marks):
    if marks >= 80:
        return 'A'
    elif marks >= 60:
        return 'B'
    else:
        return 'C'
        
n = int(input("Enter number of students: "))

for i in range(n):
    name = input(f"Enter name of student {i+1}: ")
    marks = int(input(f"Enter marks of {name}: "))
    grade = get_grade(marks)
    student = {
        "name": name,
        "marks": marks,
        "grade": grade
    }
    students.append(student)
    
print("\n--- Student Details ---")
for s in students:
    print(f"Name: {s['name']}, Marks: {s['marks']}, Grade: {s['grade']}")
    
total = sum(s['marks'] for s in students)
average = total / n

print("\nTotal Marks:", total)
print("Average Marks:", average) 
