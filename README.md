The program stores tasks in a list. You can add tasks, see all tasks, or exit. It runs until you choose to quit. Tasks are lost when the program closes.
```python
tasks = []
while True:
    print("\n1. Show tasks")
    print("2. Add task")
    print("3. Exit")

    choice = input("Choose: ")

    if choice == "1":
        if tasks:
            print("Tasks:")
            for i, task in enumerate(tasks, 1):
                print(f"{i}. {task}")
        else:
            print("No tasks yet.")
    elif choice == "2":
        task = input("Enter new task: ")
        tasks.append(task)
        print("Task added.")
    elif choice == "3":
        print("Bye!")
        break
    else:
        print("Invalid choice.")
