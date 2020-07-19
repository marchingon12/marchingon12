### Howdy, here's Austin! 😄

[![forthebadge](https://forthebadge.com/images/badges/you-didnt-ask-for-this.svg)](https://forthebadge.com)

<!--
**marchingon12/marchingon12** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# 34 

## A quiz application using JavaFX and SQLite.

----

**Goals to finish**: 
* [x] complete SQLite database for the Quiz programme. :raised_hands:
* [x] JavaFX GUI for the Quiz interface. :bowtie:
* [ ] eventually a functioning Quiz programme. :star_struck:

----

# Database
[![forthebadge](https://forthebadge.com/images/badges/built-by-developers.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/as-seen-on-tv.svg)](https://forthebadge.com)

The database used to store data for the Quiz webpage using SQLite.

## Checklist
* [x] **Make a database**
* [x] **Write some functions to connect to database**

## Important notes 
### .jar support
- compile Main.java with `javac` and use `java -cp .:sqlite-jdbc-3.30.1.jar Main` to run.
- unfortunately `-cp .:sqlite-jdbc-3.30.1.jar` is needed as a sqlite library in jar format, unless the IDE you use can implement the library. 
- **EDIT:** sqlite-jar support has been added with gradle, this should simplify things.

Known IDEs with support:  
1.  [**VSCode**](https://code.visualstudio.com/docs/java/java-project#_working-with-jar-files) 
(VSCodium - open source version of VSCode - should have support, not working at my end however)
3.  [**IntelliJ**](https://www.jetbrains.com/help/idea/library.html#define-library)



## File info
### DatabaseSingleton.java
- Connects the database with java.

### User.java
- Returns the username and answers form User.

### QuestionSet.java
- Returns the set of questions done by the User into String format.

### UserAnswer.java
- Checks the answer chosen by User. 

### Answer.java
- Returns correct answer.

### Main.java
- Code to start execution of program. Contains some examples for using code.

### sqlite-jdbc-3.30.1.jar
- Contains the sqlite library for program to run.

### quiz.db
- Data contained in database to read/write data. For table info see below.
- **Side note**: since the sqlite database isn't previewable on git, use [**SQLite Viewer**](https://inloop.github.io/sqlite-viewer/).
- All questions were either taken from https://www.fragespiel.com or https://www.opentdb.com (Translated to German using Google Translate and self-translatoin)


## Table info
-  ### Question

| Name        | Type     | Description                          |
| ----------- | -------- | ------------------------------------ |
| question_id | INTERGER | create id for each question          |
| question    | TEXT     | questions for User to answer         |
| category    | TEXT     | the category for each question genre |


-  ### Question_choices

| Name           | Type     | Description                                                  |
| -------------- | -------- | ------------------------------------------------------------ |
| choice_id      | INTERGER | create id for each choice                                    |
| question_id    | INTERGER | id of question to identify choice options for which question |
| choice         | TEXT     | choices for User to pick to answer question                  |
| correct_answer | INTERGER | true/false identification for right/wrong answer             |

-  ### User

| Name     | Type     | Description                   |
| -------- | -------- | ----------------------------- |
| user_id  | INTERGER | create id for each User       |
| username | TEXT     | Username to show name of User |

-  ### User_answer

| Name        | Type     | Description                                              |
| ----------- | -------- | -------------------------------------------------------- |
| user_id     | INTERGER | id from User to identify which User made a choice        |
| question_id | INTERGER | id from question to identify which question was answered |
| choice_id   | INTERGER | id from choice to identify which choice made by User     |

This project has been a great learning experience, stay safe y'all!! :mask: :heart:
