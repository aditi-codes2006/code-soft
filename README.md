# task_1  To_do_list
class ToDoList:
    def _init_(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)
        print(f'Task "{task}" added.')

    def update_task(self, index, new_task):
        if 0 <= index < len(self.tasks):
            old_task = self.tasks[index]
            self.tasks[index] = new_task
            print(f'Task "{old_task}" updated to "{new_task}".')
        else:
            print('Invalid task index.')

    def delete_task(self, index):
        if 0 <= index < len(self.tasks):
            removed_task = self.tasks.pop(index)
            print(f'Task "{removed_task}" deleted.')
        else:
            print('Invalid task index.')

    def list_tasks(self):
        if not self.tasks:
            print('No tasks in the list.')
        else:
            print('To-Do List:')
            for i, task in enumerate(self.tasks):
                print(f'{i + 1}. {task}')

# Example usage
if _name_ == '_main_':
    todo = ToDoList()
    todo.add_task('Complete Python internship tasks')
    todo.add_task('Review code')
    todo.list_tasks()
    todo.update_task(1, 'Review Python code')
    todo.list_tasks()
    todo.delete_task(0)
    todo.list_tasks()
