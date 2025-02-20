# expense_tracker
A simple python based expense tracker with classes for managing expenses and a database
Expense_Tracker Project



Description


The Expense Tracker is a Python-based application designed to help manage individual financial expenses. It provides two main classes:
 1. Expense Class: Represents an individual financial expense, storing attributes such as the expense’s title, amount, creation date, and last update date.
 2. ExpenseDB Class: Manages a collection of Expense objects, offering methods to add, remove, and retrieve expenses based on their ID or title.

This project helps track expenses, allowing you to update expenses, search for them, and store them in a dictionary format.

Features
 • Expense Class:
 • Stores attributes: id, title, amount, created_at, and updated_at.
 • Methods include: update() to update title and/or amount, and to_dict() to convert the expense to a dictionary.
 • ExpenseDB Class:
 • Manages a collection of Expense objects.
 • Methods include: add_expense() to add expenses, remove_expense() to delete expenses, get_expense_by_id() to fetch an expense by its ID,
get_expense_by_title() to search expenses by title, and to_dict() to convert the database into a list of dictionaries.




How to clone the repository


Start by cloning this repository to your local machine:

git clone https://github.com/your-username/expense-tracker.git

Replace your-username with your actual GitHub username.

Navigate to the Project Directory
cd expense-tracker

After cloning, change into the project directory

Install Python and run the Code




How to run the code


To run the code and test the functionality, use the following command:

python expense_tracker.py

Modify and Test the Code

Feel free to modify the code as needed, such as adding more attributes to the Expense class or introducing new methods for querying expenses.
You can also test various scenarios, like adding or removing expenses, by updating the script.


Example Usage

Here is an example of how the Expense and ExpenseDB classes can be used:

# Create an ExpenseDB instance
expense_db = ExpenseDB()

# Create and add expenses
expense1 = Expense("Groceries", 50.75)
expense_db.add_expense(expense1)

expense2 = Expense("Rent", 1200.00)
expense_db.add_expense(expense2)

# Update an expense
expense1.update(title="Groceries & Snacks", amount=55.00)

# Retrieve an expense by ID
expense = expense_db.get_expense_by_id(expense1.id)
print(expense.to_dict())

# Retrieve expenses by title
groceries_expenses = expense_db.get_expense_by_title("Groceries & Snacks")
for exp in groceries_expenses:
    print(exp.to_dict())

# Convert the entire database to a dictionary
print(expense_db.to_dict())

# Remove an expense
expense_db.remove_expense(expense1.id)


Contributing

If you’d like to contribute to this project, please fork the repository, make your changes,
and submit a pull request. Be sure to include any relevant updates to the README.md file and follow standard best practices.
