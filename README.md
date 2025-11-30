C Quiz Arena
This is a simple command-line Multiple Choice Question (MCQ) quiz application written in C. It features a hardcoded question bank and uses the Fisher-Yates shuffle algorithm to present a randomized set of 10 questions to the user.
Features
 * Extensive Question Bank: Includes 50 questions focused on C programming fundamentals.
 * Randomization: Questions are shuffled and the user is presented with 10 random questions from the bank on each run.
 * Scoring: Tracks the user's score and displays the final score and percentage at the end.
 * Simple I/O: Easy-to-use command-line interface.
Prerequisites
To compile and run this program, you need a C compiler (like GCC) installed on your system.
How to Compile and Run
Follow these steps to compile and execute the quiz on a Linux/macOS terminal or a Windows command prompt with GCC installed.
 * Save the Code: Save the provided C code into a file named quiz.c.
 * Compile: Open your terminal or command prompt and use the GCC compiler to compile the file:
   gcc quiz.c -o quiz

 * Run: Execute the compiled program:
   ./quiz

   (On some Windows systems, you may need to run quiz.exe)
Code Overview
1. Structure Definition
The struct Question holds all the data for a single MCQ, including the question text, four options, and the single-character correct answer ('A', 'B', 'C', or 'D').
struct Question {
    char question[200];
    char optionA[100];
    char optionB[100];
    char optionC[100];
    char optionD[100];
    char correctAnswer;
};

2. Randomization (Shuffle)
The shuffleQuestions function implements the Fisher-Yates (Knuth) Shuffle algorithm. This ensures that the questions array (questionBank) is thoroughly randomized, making each quiz run unique.
 * It uses srand(time(NULL)) in main to seed the random number generator, ensuring different results each time the program runs.
 * It iterates from the last element down to the second, swapping each element with a randomly chosen element before it.
3. Main Logic (main function)
 * Initialization: The questionBank array is initialized with 50 hardcoded questions.
 * Shuffling: shuffleQuestions(questionBank, 50) is called to randomize the entire bank.
 * Quiz Loop: A for loop runs 10 times to present the first 10 questions from the now-shuffled array.
 * Input/Check: It prompts the user for an answer, converts lowercase input to uppercase, and compares it against the stored correctAnswer.
 * Result: The final score and percentage are calculated and displayed.
