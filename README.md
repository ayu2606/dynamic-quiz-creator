# Dynamic Quiz Creator & Evaluator

A menu-driven **C programming project** that allows teachers to create
and manage multiple-choice questions, students to take randomized timed
quizzes, and teachers to review performance through individual reports
and class statistics.

## Features

### Teacher

-   Add multiple-choice questions with four options.
-   Set the correct option and marks for each question.
-   View all questions in the question bank.
-   Delete questions from the question bank.
-   Load five built-in sample questions.
-   Save the question bank to `questions.txt`.
-   Load questions from `questions.txt`.

### Student

-   Enter a student name before starting a quiz.
-   Choose how many questions to attempt.
-   Set a quiz time limit (1--120 minutes).
-   Receive questions in randomized order using the Fisher--Yates
    shuffle.
-   Answer with options `1`--`4`, or enter `0` to skip.
-   Receive an automatically calculated score when the quiz ends.

### Reports and results

-   View an individual student's detailed report.
-   View reports for all students.
-   See per-question feedback, including correct, incorrect, and
    unanswered questions.
-   View the class average and top performers.
-   View a leaderboard, with faster completion used to break score ties.
-   Save reports and class statistics to `results.txt`.

## Requirements

-   A C compiler, such as GCC.
-   A terminal or command prompt.

The program uses standard C library headers: `stdio.h`, `stdlib.h`,
`string.h`, and `time.h`.

## Build

Save the source code as `main.c`, then compile it with GCC:

``` bash
gcc main.c -o quiz
```

For additional compiler warnings, use:

``` bash
gcc -Wall -Wextra -std=c11 main.c -o quiz
```

## Run

### Linux / macOS

``` bash
./quiz
```

### Windows (Command Prompt)

``` cmd
quiz.exe
```

## How to use

1.  Start the program.
2.  Choose **Teacher: manage questions** to add questions, load sample
    questions, or manage the question bank.
3.  Save the question bank if you want to use it in a later session.
4.  Choose **Student: take quiz** and enter the student's name.
5.  Select the number of questions and the time limit.
6.  Answer each question using `1`, `2`, `3`, or `4`. Enter `0` to skip.
7.  Open **Reports** to review performance and class statistics.
8.  Choose **Save results to file** to write the reports to
    `results.txt`.

## Generated files

  -----------------------------------------------------------------------
  File                                Purpose
  ----------------------------------- -----------------------------------
  `questions.txt`                     Stores the question bank when the
                                      teacher saves it.

  `results.txt`                       Stores student reports and the
                                      class summary when results are
                                      saved.
  -----------------------------------------------------------------------

Both files are created in the program's current working directory.

## Concepts demonstrated

-   Structures (`struct`) for questions and student results.
-   Dynamic memory allocation using `malloc`, `calloc`, and `realloc`.
-   Arrays and pointers.
-   File handling using `fopen`, `fgets`, and `fprintf`.
-   Input validation.
-   Randomization using the Fisher--Yates shuffle.
-   Time measurement using `time` and `difftime`.
-   Sorting results for the leaderboard.

## Notes

-   The question bank and student results are held in memory while the
    program runs.
-   The question bank can be saved to and loaded from `questions.txt`.
-   Student results can be exported to `results.txt`.
-   The program does not automatically load saved files at startup; use
    the relevant teacher-menu options to load the question bank.

## License

No license has been specified for this project.
