# Ex_10_Animation
Develop an application to perform different animations for the given image on the Screen

## AIM:
To create and design an android application that perform different animations for the given image on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Create anim folder in that write coding for animation in .xml

Step 7: Perform animation function using AnimationUtil class in MainActivity.java

Step 8: Save and run the application.


## Program:
 ```
/*
Program to create and design an android application for performing different animations
Developed by: Shaik Sameer Basha
RegisterNumber:  212222240093
*/
```

## MainActivity.java:
```
package com.example.animation;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
TextView txtAnim;
Button btn1,btn2,btn3,btn4;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        txtAnim = findViewById(R.id.textv);
        btn1 = findViewById(R.id.btnScale);
        btn2 = findViewById(R.id.btnrotate);
        btn3 = findViewById(R.id.btnalpha);
        btn4 = findViewById(R.id.btntranslate);



        btn1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation move = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.move);
                txtAnim.startAnimation(move);
            }
        });
        btn2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Animation rotate = AnimationUtils.loadAnimation(getApplicationContext(),R.anim.rotate);
                txtAnim.startAnimation(rotate);
            }
        });
        btn3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Animation alpha = AnimationUtils.loadAnimation(getApplicationContext(),R.anim.alpha);
                txtAnim.startAnimation(alpha);
            }
        });
        btn4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Animation translate = AnimationUtils.loadAnimation(getApplicationContext(),R.anim.translate);
                txtAnim.startAnimation(translate);
            }
        });

    }
}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/textv"
        android:text="Shaik Sameer Basha"
        android:textSize="32sp"
        android:layout_centerInParent="true"
        android:textStyle="bold"
        android:textColor="#EDE496"/>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:layout_alignParentBottom="true">
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:id="@+id/btnScale"
            android:layout_weight="1"
            android:text="scale"/>
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:id="@+id/btnrotate"
            android:layout_weight="1"
            android:text="rotate"/>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <Button
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:id="@+id/btnalpha"
                android:layout_weight="1"
                android:text="alpha"/>
            <Button
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:id="@+id/btntranslate"
                android:layout_weight="1"
                android:text="translate"/>
        </LinearLayout>
    </LinearLayout>

</RelativeLayout>
```

## zoom.xml
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
<scale
    android:fromXScale="1"
    android:fromYScale="1"
    android:toXScale="2"
    android:toYScale="2"
    android:duration="4000"
    android:repeatCount="infinite"
    android:pivotX="50%"
    android:pivotY="50%"
    android:repeatMode="reverse"/>
</set>
```
## slide.xml
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
    <!--android:interpolated="@android:anim/bounce_interpolator"-->

    <translate android:fromXDelta="0"
        android:toXDelta="400"
        android:duration="4000"
        android:repeatCount="infinite"
        android:repeatMode="reverse"/>

</set>
```
## clockwise.xml
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
    <rotate android:fromDegrees="0"
        android:toDegrees="3600"
        android:duration="1200"
        android:pivotX="50%"
        android:pivotY="50%"/>

</set>
```
## fade.xml
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
<alpha android:fromAlpha="0"
    android:toAlpha="1"
    android:duration="4000"
    android:repeatCount="infinite"/>
</set>
```
## blink.xml
```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
<alpha android:fromAlpha="0"
    android:toAlpha="1"
    android:duration="4000"
    android:repeatCount="infinite"/>
</set>
```
## animation.xml

## Output:
![9 1](https://github.com/shaikSameerbasha5404/Ex_10_Animation/assets/118707756/1f249c4a-e6da-4243-b9b9-3eb104d7812d)
![9 2](https://github.com/shaikSameerbasha5404/Ex_10_Animation/assets/118707756/a3884839-47dc-4797-9b8a-01bf40d7aa0d)
![9 3](https://github.com/shaikSameerbasha5404/Ex_10_Animation/assets/118707756/d1d664e9-7346-46f2-992a-f73e97ea966f)

![9 4](https://github.com/shaikSameerbasha5404/Ex_10_Animation/assets/118707756/5b828ecd-6ddc-42d3-8ef1-fcbb5dc58c3c)

## Result:
Thus a Simple Android Application to perform different animations for the image on the screen using Android Studio was developed and executed successfully.
