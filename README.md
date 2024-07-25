# Quiz-App
Kairiz Cyber Technologies Internship Task
Android Studio: It provides the necessary tools for designing, coding, debugging, and testing Android applications.  Java: The primary programming language used for developing the app's logic and functionality.  XML: Used for designing the user interface (UI) layout of the app.

## Quiz App Report

### Introduction

The Quiz App, titled **"Technology Awareness Quiz,"** is designed to test users' knowledge of various technological topics. The app provides an interactive platform where users can engage with questions to assess their understanding of technology-related concepts.

### Objective

The main objective of this app is to provide users with an engaging and informative quiz experience. The app is designed to:

1. Enhance users' knowledge of technology.
2. Provide an intuitive and user-friendly interface for taking quizzes.
3. Allow users to start quizzes with ease through interactive elements.

### Features

1. **User Interface**
   - The app features a clean and visually appealing user interface, which includes a title and interactive elements such as buttons and text views.
   - The layout is optimized for user engagement, with a centered and organized structure.

2. **Quiz Functionality**
   - The quiz can be started by clicking on either the "Play" button or the associated image button.
   - Upon starting the quiz, users are presented with a series of technology-related questions.
   - The app is designed to handle user interactions smoothly, with methods in place to respond to user input.

### Implementation Details

#### Layout Design (XML)

The layout of the Quiz App is defined in the `activity_main.xml` file. Here are the key components:

- **LinearLayout**: The main container for the app's UI components, oriented vertically and centered on the screen.
- **TextView**: Displays the title of the quiz app, "Technology Awareness Quiz," in a large and prominent font size (50sp) with a light blue color.
- **ImageButton**: Represents the "Play" button with a custom drawable background, allowing users to start the quiz.
- **TextView (Play)**: An additional clickable text that allows users to start the quiz by clicking on the word "Play." It is styled in green with a font size of 40sp.

Below is the code snippet for the XML layout:

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:background="#e8f4f8"
    android:gravity="center"
    android:orientation="vertical">

    <!-- Create a TextView to show the title. -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:text="Technology Awareness Quiz"
        android:textColor="@android:color/holo_blue_light"
        android:textSize="50sp" />

    <!-- Create an ImageButton for starting the game. -->
    <ImageButton
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:background="@drawable/play"
        android:onClick="startGame" />

    <!-- Also create a TextView to show the text "Play" -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Play"
        android:textSize="40sp"
        android:textColor="@android:color/holo_green_dark"
        android:onClick="startGame" />
</LinearLayout>
```

#### Main Activity (Java)

The main logic for the quiz app is implemented in the `MainActivity.java` file. Here are the key components:

- **startGame() Method**: This method is triggered when the user clicks the "Play" button or text. It initiates the quiz by navigating to the quiz question screen or logic.

- **Question Handling**: The app presents a series of questions, each with multiple choices. Users select their answers, and the app provides feedback.

Below is a brief overview of the Java code structure:

```java
package com.example.quizapp;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    // Method to start the game when the play button is clicked
    public void startGame(View view) {
        Intent intent = new Intent(this, QuizActivity.class);
        startActivity(intent);
    }
}
```

### Conclusion

The Technology Awareness Quiz App provides a streamlined and engaging experience for users interested in testing and expanding their technology knowledge. With its simple yet effective UI and interactive quiz functionality, the app is a valuable educational tool.

