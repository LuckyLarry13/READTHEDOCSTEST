Welcome to SpeakEasy
===================================
"Speakeasy" is a language learning app designed to make learning a new language fun, interactive, and effective. With its user-friendly interface and innovative features, Speakeasy aims to break down the barriers to language acquisition.

Link to code via Github: https://github.com/SETAP-Speakeasy/Coursework

.. note::

   This project is under active development.

Our Scope
=============
We aimed to develop a user-friendly language learning app that caters to learners of varying proficiency levels. Initially, we envisioned an adaptable platform that would offer a personalized learning experience by adjusting to each user's unique needs. Our initial vision included several ambitious features:

- Adaptive difficulty that responds to user performance, emphasizing improvement areas while reinforcing strengths.
- Speech recognition for enhancing pronunciation.
- Instant definitions for selected words or phrases.
- Integration of various APIs for accurate translations across languages.
- Gamification elements like a leaderboard, streak system, and mini-games.
- A communication feature to connect users with others learning the same language or bilingual speakers.

Over time, we've scaled back our ambitions to more achievable goals, implementing a simplified version of our original plan. We have successfully integrated gamification through leaderboard and streak systems. Although our initial concept was complex and resource heavy, our final program offers essential functionality with a clean design and maintainable architecture, allowing for future development.


Our user requirements
===========================
Gamification
Users want several learning modes to be able to choose the way in which they learn.

Users also desired other gamification elements, such as leaderboards, and a “score” system that were also popular with participants, in particular the ability to compare progress to friends and peers was seen as an upside.

Users expressed a desire for more engagement and motivation from the application, as they felt they weren’t being encouraged to keep using the app enough. Notifications were seen as a positive feature, so long as they were not overwhelming.

Spelling and Grammar
Users wanted a way to understand the spelling, punctuation and grammar of their chosen language. 
Users frequently expressed how they had issues with spelling and grammar, as they felt other applications would tell them when their spelling/grammar was wrong, but not why.

Users expressed a desire for features that would have simple infographics to teach them spelling and grammar rules, including things like verb endings, conjugations, pronouns, etc.

Target Audience
Users want to have their difficulty adjusted to them, as we had a wide variety of participants across skill levels, with the majority being beginner users.
Users should be treated equally, making sure the leaderboard/score systems are the same for all.

Progress Tracking and Feedback
Users want a way to track progress, as many felt they were unsure of how effectively they were studying, and whether or not they were progressing at a solid pace.

Usability and Accessibility
Users want an easily usable and accessible app, designed with the user in mind, where you can easily find your way around and get to any part of the app in as few button presses as possible.
Social Features and Community Building
Users wanted a wide some social features e.g. leaderboards 
Language
Users want several ways to learn their chosen language, ranging from quizzes to flashcards and. conversation practice.
Users want a variety of speeds to learn at, both quick-fire shorter questions and longer conversations.
Users wanted to have their difficulty adjust to how well they’re doing, if participants are stuck the questions should get easier, and vice versa.

--NOTE NOT SOME OF THESE REQUIREMENTS HAVE CHANGED SINCE THE FIRST SUBMISSION DUE TO SCOPE, TIME AND RESOURCES.

Elements of Implementation
==========================
This section outlines the code architecture setup:

Assets/images
-------------
Used to store images and other assets.

Lib
---
This directory includes several subdirectories and files:

Database
^^^^^^^^
Contains SQL scripts:
- ``createtables.sql``: Script to create tables.
- ``droptables.sql``: Script to drop tables.
- ``insert.sql``: Script for inserting data.
- ``queries.sql``: Script containing SQL queries.

Screens
^^^^^^^
Contains Dart files for different screens in the application:
- ``exportScreens.dart``: Manages screen exports for better readability.
- ``LeaderboardPage.dart``: Displays the global leaderboard with usernames, scores, and rankings.
- ``LearnScreen.dart``: Offers a choice between quiz and study modes.
- ``LoginScreen.dart``: Manages login and sign-up processes, including backend interactions.
- ``MenuScreen.dart``: Serves as the landing page of the application.
- ``QuizScreen.dart``: Hosts the quiz mode where users test their knowledge to score points and advance in ranks.
- ``SettingsPage.dart``: Provides a basic settings page (currently without functionality).
- ``StudyScreen.dart``: Another game mode screen that assists users with questions.

Globals.dart
^^^^^^^^^^^^
Contains definitions for all global variables used across the application.

Main.dart
^^^^^^^^^
The primary script used to run the application.


How to set up
===================
Windows
^^^^^^^
To start, download Dart: https://dart.dev/get-dart
Then, flutter: https://docs.flutter.dev/get-started/install
Setup an android emulator (Android Studio) or use an Android device plugged or in any IDE, and use the "run feature" in any of these to run the program

Arch Linux
^^^^^
To start, download Dart: ``pacman -S dart``
Then, flutter: ``pacman -S flutter``
Setup an android emulator (Android Studio: https://aur.archlinux.org/android-studio.git) or use an Android device plugged or in any IDE, and use the "run feature" in any of these to run the program



Main Components
===============
We have several main components:
------------------
- Login system
- Main Menu
- Study
- Quiz
- Leaderboard

The user starts by either logging in or signing up in our system. If they log in, their data is stored in our Postgres cloud database, or they can input their details to create a new account. This process is quick and user-friendly. Once logged in, the user is directed to the Main Menu screen, which offers several options. One option is the Study mode, our simplest game mode. Here, users are given a question and must choose the correct answer from four possibilities. A correct answer prompts a congratulatory message, while an incorrect one triggers a notification of their error. This interactive feedback is designed to keep the user engaged and learning.

After completing Study mode, users can move on to Quiz mode. This mode follows the same format but includes tracking of correct answers and scoring. After ten correct answers, users advance to the next level, from Level 1 (the easiest) to Level 5 (the hardest). They receive a score for that session and a total score that accumulates over time. This scoring system motivates users to improve their performance over time.
Their overall score is recorded in the database and displayed on the Leaderboard, which shows the user's total score alongside the top ten users on the app. The Leaderboard is not just a tool for recognition but also sparks competitiveness among users, encouraging them to do better and climb the rankings.



