<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D GUI with News Ticker</title>
    <style>
        /* Body and general layout */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: #f0f0f0;
        }

        /* Header with scrolling text (news ticker) */
        .header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            position: relative;
            overflow: hidden;
        }

        .ticker {
            position: absolute;
            white-space: nowrap;
            animation: scroll 15s linear infinite;
            font-size: 1.5em;
            padding-left: 100%;
        }

        @keyframes scroll {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(-100%);
            }
        }

        /* 3D table design */
        .table-container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }

        table {
            width: 80%;
            border-collapse: collapse;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
            overflow: hidden;
            background-color: white;
        }

        th, td {
            padding: 15px;
            text-align: center;
            border: 1px solid #ddd;
        }

        th {
            background-color: #4CAF50;
            color: white;
            font-size: 1.2em;
        }

        tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        tr:hover {
            background-color: #f1f1f1;
            transform: scale(1.02);
            transition: 0.2s;
        }
    </style>
</head>
<body>

    <!-- Header with moving news ticker -->
    <div class="header">
        <div class="ticker">
            Latest Tech Updates: AI Revolution in Healthcare, Quantum Computing Breakthrough, New VR Headsets Released, 5G Expands Globally, SpaceX Mars Mission Plans.
        </div>
    </div>

    <!-- 3D Table Example -->
    <div class="table-container">
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
                    <td>AI Integration</td>
                    <td>Completed</td>
                </tr>
                <tr>
                    <td>Feature 2</td>
                    <td>Blockchain Security</td>
                    <td>In Progress</td>
                </tr>
                <tr>
                    <td>Feature 3</td>
                    <td>Cloud Computing</td>
                    <td>Pending</td>
                </tr>
            </tbody>
        </table>
    </div>

    <script>
        // JavaScript could be added here for more dynamic effects or features
    </script>

</body>
</html>
