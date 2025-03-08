<!DOCTYPE html>
<html lang="en">
  <head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Test</title> 
    <style>
      body { 
        font-family: Arial, sans-serif; margin: 20px;
      } .question {
        margin-bottom: 20px; 
      } 
      label { 
        font-size: 1.2em;
      } input[type="text"] { 
        margin-left: 10px;
        padding: 5px; 
        font-size: 1em;
      } 
      button { 
        margin-top: 20px; 
        padding: 10px 20px; 
        font-size: 1em; 
        cursor: pointer;
      }
      .result {
        margin-top: 20px;
        font-size: 1.2em; 
      } </style> 
  </head>
  <body> 
    <h1>Math Test</h1>
    <form id="mathTest"> 
      <h2>Start Test
        <h3>Name: _______
      <!-- Question 1: Word Problem --> <div class="question">
        <label for="q1">1. If John has 5 apples and gives 2 to his friend, how many apples does he have left?</label> 
        <input type="text" id="q1" name="q1"> 
      </div> <!-- Question 2: Math Symbol (+) --> 
      <div class="question">
        <label for="q2">2. What is 8 + 5?</label>
        <input type="text" id="q2" name="q2">
      </div> 
      <!-- Question 3: Math Symbol (-) --> 
      <div class="question">
        <label for="q3">3. What is 15 - 7?</label> 
        <input type="text" id="q3" name="q3">
      </div> 
      <!-- Question 4: Math Symbol (*) --> 
      <div class="question">
        <label for="q4">4. What is 6 * 4?</label>
        <input type="text" id="q4" name="q4">
      </div> 
      <!-- Submit Button -->
      <button type="button" onclick="checkAnswers()">Submit</button> 
    </form>
    <div id="result" class="result"></div>
    <script> 
      function checkAnswers() {
        // Get the user's answers
        var q1Answer = document.getElementById('q1').value;
        var q2Answer = document.getElementById('q2').value;
        var q3Answer = document.getElementById('q3').value; 
        var q4Answer = document.getElementById('q4').value;
        // Correct answers 
        var correctAnswers = { 
          q1: "3", 
          q2: "13", 
          q3: "8", 
          q4: "24" 
        };
        var score = 0;
        var feedback = ''; 
        // Check each answer 
        if (q1Answer === correctAnswers.q1) score++; 
        if (q2Answer === correctAnswers.q2) score++;
        if (q3Answer === correctAnswers.q3) score++;
        if (q4Answer === correctAnswers.q4) score++; 
        // Display result 
        if (score === 4) {
          feedback = "Excellent! You got all the answers correct!";
        } else { 
          feedback = "You got " + score + " out of 4 correct.";
        } document.getElementById('result').innerHTML = feedback;
      } 
    </script> 
  </body> 
</html>
