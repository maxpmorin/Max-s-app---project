Flashcard App

A simple Android flashcard application built with Kotlin and XML layouts.
The app shows one multiple-choice question and lets the user pick an answer. Correct answers turn green, and wrong answers turn red while highlighting the correct one.



Features

- [x]	One flashcard question: “Who is the 44th President of the United States?”

- [x]	One multiple-choice question with 3 answers: Bill Clinton, George Bush, Barack Obama

- [x]	Correct answer turns green

- [x]	Wrong answer turns red, while the correct answer is highlighted green

- [x]	Once an answer is picked, all choices are disabled



Project Structure

app/

 ├ src/
 
        ├ main/
        
                 ├ java/com/example/maxsflashcard/MainActivity.kt
                 
                 ├ res/
                 
                        ├ layout/activity_main.xml



Layout (activity_main.xml)

•	TextView with ID flashcard_question → Shows the question.

•	TextView with ID choice_clinton → First option.

•	TextView with ID choice_bush → Second option.

•	TextView with ID choice_obama → Third option.



Main Code (MainActivity.kt)

onCreate()

•	Loads the XML layout using setContentView().

•	Connects the Kotlin variables (choiceClinton, choiceBush, choiceObama) to their corresponding TextViews in the XML using findViewById().

•	Sets up click listeners:

o	Clinton & Bush → wrong (red).

o	Obama → correct (green).

markAnswer(view: TextView, isCorrect: Boolean)

•	If correct → Colors the chosen answer green.

•	If wrong → Colors the chosen answer red and also highlights the correct one (Obama) in green.

•	Calls disableChoices() to prevent multiple taps.

disableChoices()

•	Sets .isEnabled = false for all three answers, meaning you can’t change your answer after selecting once.



Future Improvements

•	Adding multiple flashcards.

•	Implementing “Next Question” button.

•	Adding animations for correct/wrong answers.

