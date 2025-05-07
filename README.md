<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            overflow: hidden;
        }
        th, td {
            padding: 15px;
            text-align: center;
            border: 1px solid #ddd;
        }
        th {
            background-color: #4CAF50;
            color: white;
        }
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        tr:hover {
            background-color: #ddd;
        }
        td {
            background-color: #fff;
            transition: transform 0.3s ease;
        }
        td:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <table>
        <thead>
            <tr>
                <th>Feature</th>
                <th>Description</th>
                <th>Status</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Feature 1</td>
                <td>Description of Feature 1</td>
                <td>Completed</td>
            </tr>
            <tr>
                <td>Feature 2</td>
                <td>Description of Feature 2</td>
                <td>In Progress</td>
            </tr>
            <tr>
                <td>Feature 3</td>
                <td>Description of Feature 3</td>
                <td>Pending</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
