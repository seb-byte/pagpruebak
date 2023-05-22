# pagpruebak

<!DOCTYPE html>
<html>
<head>
    <title>Expense Tracker</title>
    <style>
        /* CSS styling */
        body {
            font-family: Arial, sans-serif;
        }
        h1 {
            text-align: center;
        }
        #expense-form {
            margin: 20px auto;
            width: 300px;
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
        }
        #expense-form input[type="text"],
        #expense-form input[type="number"],
        #expense-form input[type="submit"] {
            display: block;
            margin: 10px 0;
            width: 100%;
        }
        #expense-list {
            margin: 20px auto;
            width: 300px;
        }
        #expense-list li {
            list-style: none;
            margin-bottom: 5px;
            padding: 5px;
            background-color: #f5f5f5;
        }
    </style>
</head>
<body>
    <h1>Expense Tracker</h1>

    <div id="expense-form">
        <input type="text" id="expense-name" placeholder="Expense Name">
        <input type="number" id="expense-amount" placeholder="Amount">
        <input type="submit" value="Add Expense" onclick="addExpense()">
    </div>

    <ul id="expense-list"></ul>

    <script>
        // JavaScript functionality
        function addExpense() {
            var expenseName = document.getElementById("expense-name").value;
            var expenseAmount = document.getElementById("expense-amount").value;

            var expenseItem = document.createElement("li");
            expenseItem.textContent = expenseName + ": $" + expenseAmount;

            document.getElementById("expense-list").appendChild(expenseItem);

            // Clear input fields
            document.getElementById("expense-name").value = "";
            document.getElementById("expense-amount").value = "";
        }
    </script>
</body>
</html>
