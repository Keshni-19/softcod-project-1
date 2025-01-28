# softcod-project-1
tasks = []


def addTask():
  task = input("Enter a task: ")
  tasks.append(task)
  print(f"The task '{task}' has been added to the list.")
  
def listTasks():
  if not tasks:
    print("No tasks are in the list.")
  else:
    print("Current Tasks: ")
    for index, task in enumerate(tasks):
      print(f"Task {index}. {task}")
      
def deleteTask():
  listTasks()
  try:
    taskToDelete = int(input("Enter the task to be deleted: "))
    if taskToDelete >= 0 and taskToDelete < len(tasks):
      tasks.pop(taskToDelete)
      print(f"The tasks {taskToDelete} has been deleted. ")
    else:
      print("Invalid input.")
  except:
    print("Invalid input.")
    
if __name__ == "__main__":
  while True:
    print("Enter one of the options")
    print("1. Add a task")
    print("2. List all the tasks")
    print("3. Delete a task")
    print("4. Exit")
    choice = input("Enter your option: ")
    if choice == "1":
      addTask()
    elif choice == "2":
      listTasks()
    elif choice == "3":
      deleteTask()
    elif choice == "4":
      break
    else:
      print("Invalid input. Try again.")
print("Thank you :)")    
    
