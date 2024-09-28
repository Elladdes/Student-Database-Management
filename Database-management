#student_database is a preform list of pre-existing students
student_database = [['kevin', ['Pre-calculus 12', 'English 12', 'CLC', 'Mandarin', 'AP CSP'], 88], ['HYUNG',['Physics 11', 'English 11', 'PE 10', 'AP CSP', 'Pre-calculus 11'], 88], ['Ali',['AP physics', 'AP calculus',  'AP CSP', 'English 12'], 90], ['Chau Anh NGUYEN',['AP Calculus', 'English 12', 'CLE', 'AP CSP', 'Chemistry 11'], 99], ['Artin', ['Pre-calculus 12', 'Chemistry 11', 'AP CSP', 'CLC', 'English 11'], 80], ['Elahe',['Physics 12', 'CLE', 'English 11', 'AP CSP', 'MHC'], 95], ['YUNALA KIM', ['Physics 11', 'MHC', 'AP CSP', 'English 11', 'band'], 90], ['Khin PYAE SONE HTET', ['AP CSP', 'English 12', 'CLE', 'Pre-calculus 12', 'Social Studies 10'], 87], ['Erfan', ['chemistry 12', 'Calculus 12', 'AP CSP', 'English 12'], 78], ['Anna', ['AP CSP', 'Pre-calculus 12', 'Physics 11', 'English 11', 'Engineering 11'], 89], ['Parsa',['AP CSP', 'English 12', 'Economics 12', 'Chemistry 12'], 67], ['JUNGYEOP SHIN', ['AP CSP' , 'MHC', 'Physics 11', 'English 11', 'Band'], 78]]
#student_subjects is a preform list of pre-existing students' subjects, globa variable
student_subjects = []
#grades is a preform list of pre-existing grades, global variable
grades = []
'''the function add_student(), assigns a value as an input to the variable 'name'
#it asks for the number of the subjects the student has and assigns a value as an input to the variable 'num_subjects'
#the number assigned to num_subjects is used to determine how many times the loop will run
#the loop will ask for a subject name and assign a value as an input to the variable 'subject'and appends the list 'student_subjects'
#within the loop the variable i which is the number of the subject will be formatted into a string and is assigned to the variable 'subject'
#the variable student_data is assigned to a list of the variable name and the list student_subjects and the grade average as the third index
#which will then be appended to the list student_database'''
def add_student():
  name = input("Enter the name of the student: ")
  num_subjects = int(input("Enter the number of subjects: "))
  for i in range(1, num_subjects + 1):
    subject = input(f"Enter subject number {i}: ")
    student_subjects.append(subject.capitalize())
  grade = int(input("Enter the grade average: "))
  student_data = [name.capitalize(), student_subjects, grade]
  student_database.append(student_data)
  print("Student added!")

'''the function display_students() prints the student_database list. If student_database is equal to an empty list, it will print "No students in the database", if student_database is not equal to an empty list, it will go to else, and for each element in student_database, it will print the element which different indexes are formatted as a string'''
def display_students():
  if student_database == []:
    print("No students in the database.")
  else:
    for student in student_database:
      print(f"name: {student[0]}\nsubjects: {student[1]}\ngrade: {student[2]}\n")

'''The funtion grade_average() inputs a values for the variable name and then iterates through the list student_database. If the first index of the element in the list is equal to the capitalized format of the name inputted by the user, it will print the formatted indexes of the variables as a string'''
def grade_average():
  name = input("Enter the name of the student for grade average:")
  for student in student_database:
    if student[0] == name.capitalize():
      print(f"The average grade for {student[0]} is {student[2]}")

'''the function subject_search() allows to search for an subject that who is taking that subject and print out their names. In the function, it asks for one subject that user wants to check. For each element in student_database, if the subject that user input is equal to the second index of the element, it will add the element (the first index of student is formatted) in the list students_taking_that_subject. And it will format and print all the elements that are in the list students_taking_that_subject'''
students_taking_that_subject = []
def subject_search():
  subject = input("Enter the subject to search for: ")
  for student in student_database:
    if subject.capitalize() in student[1]:
      students_taking_that_subject.append(f"{student[0]},")
  print(f"{students_taking_that_subject} have {subject} in their subjects.")
  
'''the function remove_student() allows to remove a student from the student_database. In the function, it asks for the name of the student that user wants to remove. For each element in student_database, if the name that user input is the first index of the element student, it will remove the element from the list student_database. And it will print "student was removed" and the while loop will break. wihtin the while loop if the name that user input is not in the list student_database the while loop won't break and it will print "student not found"'''
def remove_student():
  name = input("Enter the name of the student to remove: ")
  while True:
    for student in student_database:
      if student[0] == name.capitalize():
        student_database.remove(student)
        print("Student was removed.")
    break
  print("student not found.")
      

'''the function update_grades() allows the user to update a grade of a student. In the function, it asks for the name of the student that user wants to change their grade. For the element that is in the list student, if the name that user input is in the element, it will print the formatted version of the variable name and formats it as a string that shows the average of the student. With the while loop it will ask whether the user wants to change the average of this student, if the user input "yes" it pops the third index (average) of the student and it will ask for the new grade, and inserts it in index 2 in the element of the list student database. If the user inputs "no", it will print "Ok." and the while loop will break. If the name is not been found from the student_database, it will go to else, and will print "invalid input, please enter yes or no"'''
def update_grades():
  name = input("Enter the name of the student to see the current average: ")
  for student in student_database:
    if student[0] == name:
      print(f"Current average for {name}: {student[2]}")
      while True:
        ans = input("Do you want to change the average grade? yes or no?: ")
        if ans == "yes":
          new_average = int(input("Enter the new average grade: "))
          student.pop(2)
          student.insert(2, new_average)
          print("Grades updated.")
          print(f"The new average grade for {name} is {new_average}")
          break
        elif ans == "no":
          print("Ok.")
          break
        else:
          print("Invalid input, Please enter yes on no")

'''the function exit(), allows the user to exit the program as it will print "thank you for using the student database".'''
def exit():
  print("Thank you for using the student database!")
  
print("1. Add a student\n2. Display students\n3. Grade Average\n4. Subject Search\n5. Remove a student\n6. Update Grades\n7. Exit")

'''the funtion main() inputs a value for the variable choice and with the first if statement it will check its equality to 1 and if it is equal to 1 the funtion add_student() will be called, this goes on until number 7 with the value 7; this program will run unitl the user input 7, and the program will run the function that the user input. if the user enters a number that is not in the range of 1 to 7, it will print "invalid choice, please enter a number from 1-7".'''
def main():
  while True:
    choice = int(input("Enter your choice: "))
    if choice == 1:
      add_student()
    elif choice == 2:
      display_students()
    elif choice == 3:
      grade_average()
    elif choice == 4:
      subject_search()
    elif choice == 5:
      remove_student()
    elif choice == 6:
      update_grades()
    elif choice == 7:
      exit()
      break
    else:
      print("Invalid choice, please enter a number from 1-7")

#funtion main has been called  
main()
