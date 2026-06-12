<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dietary Survey</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f7f6;
        }
        .container {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 16px;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.3s;
        }
        button:hover {
            background-color: #45a049;
        }
        .question-box {
            display: none;
            margin-top: 20px;
            animation: fadeIn 0.5s ease;
        }
        .btn-option {
            background-color: #008CBA;
            margin: 5px;
        }
        .btn-option:hover {
            background-color: #007bb5;
        }
        #result {
            margin-top: 20px;
            font-weight: bold;
            color: #333;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <button id="startBtn" onclick="showQuestion()">Click Me</button>

    <div id="questionBox" class="question-box">
        <h3>Are you a vegetarian or not?</h3>
        <button class="btn-option" onclick="submitAnswer('Vegetarian')">Yes, I am</button>
        <button class="btn-option" onclick="submitAnswer('Not a Vegetarian')">No, I am not</button>
    </div>

    <div id="result"></div>
</div>

<script>
    function showQuestion() {
        // Hide the initial start button
        document.getElementById('startBtn').style.display = 'none';
        // Show the question box
        document.getElementById('questionBox').style.display = 'block';
    }

    function submitAnswer(answer) {
        // Hide the question box after an option is selected
        document.getElementById('questionBox').style.display = 'none';
        // Display the user's choice
        document.getElementById('result
