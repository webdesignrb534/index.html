<!DOCTYPE html>
  </head>
  <body> 
    <h1>Math Test</h1>
    <form id="mathTest"> 
      <h2>Start Test
        <h3>Name: _______
      <!-- Question 1: Word Problem --> <div class="question">
        <label for="q1">1. If John has 5 apples and gives 2 to his friend, how many apples does he have left?</label> 
        <input type="text" id="q1" name="q1"> 
        </h4>Answer here: _____
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
          <h5> End Test
</body> 
</html>
