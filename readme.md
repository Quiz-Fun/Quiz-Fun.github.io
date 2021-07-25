# Quiz Fun
System for creating, editing and managing quizes.

## Functionality
* Registering users
* Being able to browse and take quizes from other users
* Quizes with various topics
* Ability to filter quizes based on topics and search by title
* Statistics for all users and quizes
* Interactive editor for quizes
* Interactive and flexible UX

## Technologies
* HTML, CSS, JavaScript
* lit-html, page
* GitHub Pages, Back4app

## Views (Pages)
* **Welcome Screen** (landing page)
* **Login/Regsiter** - register with email, username, password
* **Quiz Browser** - list with quizes and the ablility to search by title and filter by topic
* **Quiz Details** - additional information, statistics for the quiz, information about the author and the ability to take the quiz
* **Quiz Contest Mode** - answer questions, one question displayed at a time, the ability to go to the next or previous question, the ability to restart the quiz
* **Quiz Results** - result summery, the ability to review wrongly answered questions
* **Profile Page** - information about quizes created and all quizes taken
* **Quiz Editor** - integrated editor for quizes, questions and answers

## Initialization
### Data structure
#### Collections
* Sessions
* Users
```javascript
{
    email: String,
    username: String,
    password: String
}
```
* Quizes
```javascript
{
    title: String,
    topic: String,
    questionCount: Number
}
```
* Questions
```javascript
{
    text: String,
    answers: Array<String>,
    correctIndex: Number,
    quiz:  Pointer<Quiz>
}
```
* Solutions
```javascript
{
    quiz: Pointer<Quiz>,
    correct: Number
}
```

#### Access Control
* Guests can register, view catalog, additional info for quizes and profile page for users
* Registered users can take quizes, review personal scores, create and edit quizes
* Only quiz creator can edit or delete it
* Every registered user can take a quiz