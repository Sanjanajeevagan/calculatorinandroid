# Ex.No:7 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to print the text “calculator operation”.
Developed by:Sanjana J
Registeration Number :212224230240

```
## Main activity.xml
``` python
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:layout_width="411dp"
        android:layout_height="50dp"
        android:id="@+id/editText"
        android:layout_marginTop="150dp"
        android:autofillHints=""
        android:ems="10"
        android:hint="Enter the first number"
        android:inputType="textPersonName"
        android:text=""
        android:textColor="#A125B6" />

    <EditText
        android:layout_width="411dp"
        android:layout_height="50dp"
        android:id="@+id/editText2"
        android:layout_marginTop="30dp"
        android:layout_below="@+id/editText"
        android:autofillHints=""
        android:ems="10"
        android:hint="Enter the second Number"
        android:inputType="textPersonName"
        android:text=""
        android:textColor="#A125B6" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="60dp"
        android:id="@+id/textview"
        android:gravity="center"
        android:text="Calculator"
        android:textSize="30dp"
        android:textAllCaps="true"
        android:textColor="#A125B6"
        android:textStyle="bold" />

    <Button
        android:layout_width="132dp"
        android:layout_height="62dp"
        android:id="@+id/button1"
        android:layout_below="@+id/editText2"
        android:layout_marginTop="36dp"
        android:text="+"
        android:gravity="center"
        android:layout_marginLeft="10dp" />

    <Button
        android:layout_width="132dp"
        android:layout_height="62dp"
        android:id="@+id/button2"
        android:layout_below="@+id/editText2"
        android:layout_marginTop="36dp"
        android:text="-"
        android:gravity="center"
        android:layout_marginLeft="260dp" />

    <Button
        android:layout_width="132dp"
        android:layout_height="62dp"
        android:id="@+id/button3"
        android:layout_below="@+id/button1"
        android:layout_marginTop="36dp"
        android:text="*"
        android:gravity="center"
        android:layout_marginLeft="10dp" />

    <Button
        android:layout_width="132dp"
        android:layout_height="62dp"
        android:id="@+id/button4"
        android:layout_below="@+id/button2"
        android:layout_marginTop="36dp"
        android:text="%"
        android:gravity="center"
        android:layout_marginLeft="260dp" />
</RelativeLayout>
```
## Mainactivity.java

```python

package com.example.calculator;

import android.annotation.SuppressLint;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {
    EditText et1,et2;
    TextView tv2;
    Button add,sub,mul,div;

    @SuppressLint("MissingInflatedId")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        et1 = findViewById(R.id.editText);
        et2 = findViewById(R.id.editText2);
        tv2 = findViewById(R.id.textview);
        add = findViewById(R.id.button1);
        sub = findViewById(R.id.button2);
        mul = findViewById(R.id.button3);
        div = findViewById(R.id.button4);

        add.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                double a1 = Double.parseDouble(et1.getText().toString());
                double a2 = Double.parseDouble(et2.getText().toString());
                double result = a1 + a2;
                tv2.setText(Double.toString(result));
            }
        });

        sub.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                double a1 = Double.parseDouble(et1.getText().toString());
                double a2 = Double.parseDouble(et2.getText().toString());
                double result = a1 - a2;
                tv2.setText(Double.toString(result));
            }
        });

        mul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                double a1 = Double.parseDouble(et1.getText().toString());
                double a2 = Double.parseDouble(et2.getText().toString());
                double result = a1 * a2;
                tv2.setText(Double.toString(result));
            }
        });

        div.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                double a1 = Double.parseDouble(et1.getText().toString());
                double a2 = Double.parseDouble(et2.getText().toString());
                double result = a1 / a2;
                tv2.setText(Double.toString(result));
            }
        });

    }
}
```

## OUTPUT


<img width="1772" height="985" alt="Screenshot 2025-10-07 135647" src="https://github.com/user-attachments/assets/e4bd259e-0081-41f9-8854-5f199c25dd3b" />

<img width="1809" height="999" alt="Screenshot 2025-10-07 135713" src="https://github.com/user-attachments/assets/a2ecdfc1-7a67-415c-87d6-9657559c866b" />


## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
