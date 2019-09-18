# A-Basic-calculator
This calculator has addition , Subtraction, Multiplication, Division , Square root capability













Mainactivity.java
..................
package com.example.calculatorbasic;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    public EditText edt1;
    public Button button1,button2,button3,buttonroot,button4,button5,button6,button7,button8,button9,buttonplus,buttonminus,buttonmul,buttondiv,button0,buttoneql,buttonC;
    public float mValue1,mValue2;
    public boolean Addition,Multiplication,Division,Sub;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button1 = findViewById(R.id.button1);
        button2 = findViewById(R.id.button2);
        button3 = findViewById(R.id.button3);
        button4 = findViewById(R.id.button4);
        button5 = findViewById(R.id.button5);
        button6 = findViewById(R.id.button6);
        button7 = findViewById(R.id.button7);
        button8 = findViewById(R.id.button8);
        button9 = findViewById(R.id.button9);
        buttonplus = findViewById(R.id.buttonplus);
        buttonminus=findViewById(R.id.buttonminus);
        buttondiv=findViewById(R.id.buttondiv);
        buttonmul=findViewById(R.id.buttonmul);
        edt1=findViewById(R.id.edt1);
        buttonC=findViewById(R.id.buttonC);
        buttoneql=findViewById(R.id.buttoneq);
        button0=findViewById(R.id.button0);
        buttonroot=findViewById(R.id.root);


        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"1");
            }
        });
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"2");
            }
        });
        button3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"3");
            }
        });
        button4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"4");
            }
        });
        button5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"5");
            }
        });
        button6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"6");
            }
        });
        button7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"7");
            }
        });
        button8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"8");
            }
        });
        button9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"9");
            }
        });
        button0.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText(edt1.getText()+"0");
            }
        });
        buttonplus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(edt1==null){
                    edt1.setText("");
                }
                else {
                    mValue1=Float.parseFloat(edt1.getText()+"");
                    Addition=true;
                    edt1.setText(null);
                }
            }

        });
        buttonminus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(edt1==null){
                    edt1.setText("");
                }
                else{
                    mValue1=Float.parseFloat(edt1.getText()+"");
                    Sub=true;
                    edt1.setText(null);
                }
            }
        });
        buttondiv.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(edt1==null){
                    edt1.setText("");
                }
                else {
                    mValue1=Float.parseFloat(edt1.getText()+"");
                    Division=true;
                    edt1.setText(null);
                }
            }
        });
        buttonmul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(edt1==null){
                    edt1.setText("");
                }
                else {
                    mValue1=Float.parseFloat(edt1.getText()+"");
                    Multiplication=true;
                    edt1.setText(null);
                }
            }
        });

        buttonC.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edt1.setText("");
            }
        });
        buttoneql.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                mValue2=Float.parseFloat(edt1.getText()+"");
                if(Addition==true){
                    edt1.setText(mValue1+mValue2+"");
                    Addition=false;
                }
                if(Sub==true){
                    edt1.setText(mValue1-mValue2+"");
                    Sub=false;
                }
                if(Multiplication==true){
                    edt1.setText(mValue1*mValue2+"");
                    Multiplication=false;
                }
                if(Division==true){
                    edt1.setText(mValue1/mValue2+"");
                    Division=false;
                }
            }
        });
        buttonroot.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(edt1==null){
                    edt1.setText("");
                }
                else {
                    mValue1=Float.parseFloat(edt1.getText()+"");
                    double a = (double)mValue1;
                    float b= (float)(Math.sqrt(a));
                    edt1.setText(b+"");


                }
            }
        });

    }



}




Activity.xml
................

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:layout_weight="1"
    android:background="@drawable/floor"
    tools:context=".MainActivity">

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <EditText
            android:id="@+id/edt1"
            android:layout_width="match_parent"
            android:layout_height="150dp"
            android:background="@color/colorPrimary"
            android:paddingBottom="10dp"></EditText>
    </RelativeLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1">

       <Button
           android:id="@+id/button1"
           android:layout_width="0dp"
           android:layout_height="match_parent"
           android:layout_weight="1"
           android:text="1"
           android:textSize="26dp"
           android:textColor="@color/colorPrimaryDark">
       </Button>
        <Button
            android:id="@+id/button2"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="2"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button3"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="3"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/buttoneq"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="="
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1">

        <Button
            android:id="@+id/button4"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="4"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button5"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="5"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button6"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="6"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/buttonC"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="C"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"

        android:layout_height="0dp"
        android:layout_weight="1">

        <Button
            android:id="@+id/button7"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="7"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button8"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="8"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button9"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="9"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/button0"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="0"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="^(1/2)"
            android:id="@+id/root">
        </Button>

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"

        android:layout_height="0dp"
        android:layout_weight="1">

        <Button
            android:id="@+id/buttonplus"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="+"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/buttonminus"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="-"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/buttonmul"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="*"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:id="@+id/buttondiv"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="/"
            android:textSize="26dp"
            android:textColor="@color/colorPrimaryDark">
        </Button>
        <Button
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text=".">

        </Button>

    </LinearLayout>


</LinearLayout>

