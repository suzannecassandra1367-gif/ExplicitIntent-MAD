# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: Cassandra Suzanne F
Registeration Number : 212225240027
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".SecondActivity">

    <!-- Title -->
    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="This is Second Activity"
        android:textSize="20sp"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="100dp"/>

    <!-- Button -->
    <Button
        android:id="@+id/btnGoBack"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="GO TO HOME ACTIVITY"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="50dp"/>
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.exp02explicit;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

        // Button click → Open SecondActivity
        Button btnGo = findViewById(R.id.btnGo);
        btnGo.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, SecondActivity.class);
            startActivity(intent);
        });
    }
}
```


## OUTPUT

<img width="1042" height="595" alt="image" src="https://github.com/user-attachments/assets/4753257e-d13b-4f00-a929-d653cb24b76f" />


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


