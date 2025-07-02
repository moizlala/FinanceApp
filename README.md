# FinanceApp

FinanceApp is a simple, modern web application built with ASP.NET Core Razor Pages (.NET 9) for tracking personal expenses. It allows users to add, view, and visualize their expenses by category, providing a clear overview of spending habits.

## Features

- **Add Expenses:**  
  Users can add new expenses by providing a description, amount, and category. All fields are required, and the amount must be greater than zero.

- **View Expenses:**  
  All recorded expenses are displayed in a tabular format, showing the description, amount, category, and date.

- **Expense Visualization:**  
  Expenses are summarized and visualized using a pie chart (powered by Chart.js), giving users an at-a-glance overview of spending distribution by category.

- **Responsive UI:**  
  The app uses Bootstrap for a clean, responsive interface.

## Technologies Used

- ASP.NET Core Razor Pages (.NET 9)
- Entity Framework Core (SQL Server)
- Bootstrap 5
- Chart.js (for data visualization)
- C#

## Project Structure

- **Models**
  - `Expense.cs`: Represents an expense entry with validation.
  - `ExpenseChartData.cs`: Used for chart data aggregation.
- **Controllers**
  - `ExpensesController.cs`: Handles expense CRUD operations and chart data API.
  - `HomeController.cs`: Handles home and privacy pages.
- **Views**
  - `Expenses/Index.cshtml`: Lists all expenses and displays the chart.
  - `Expenses/Create.cshtml`: Form to add a new expense.
  - `Shared/_Layout.cshtml`: Common layout with navigation.
- **Data**
  - `FinanceAppContext.cs`: EF Core DB context.
  - `IExpensesService.cs` & `ExpensesService.cs`: Service abstraction and implementation for expense operations.

## How It Works

1. **Adding an Expense:**  
   Navigate to the "Add Expense" page, fill in the required fields, and submit. The app validates the input and saves the expense to the database.

2. **Viewing Expenses:**  
   The main page lists all expenses in a table. Each entry shows its description, amount, category, and date.

3. **Visualizing Expenses:**  
   Below the table, a pie chart displays the total amount spent per category. The chart updates automatically as new expenses are added.

## Getting Started

1. **Clone the repository:**

2. **Configure the database:**
   - Update the connection string in `appsettings.json` as needed.
   - Run EF Core migrations to create the database: ```bash
     dotnet ef database update
 ```
3. **Run the application:** 
