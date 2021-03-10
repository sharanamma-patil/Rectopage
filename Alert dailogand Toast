package com.example.mycal;

import android.content.DialogInterface;
import android.os.Bundle;

import com.google.android.material.floatingactionbutton.FloatingActionButton;
import com.google.android.material.snackbar.Snackbar;

import androidx.appcompat.app.AlertDialog;
import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.widget.Toolbar;

import android.view.View;

import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    Button Add, Subtract;
    Double num1, num2, Ans;
    Textview Answer;
    EditText Num1, Num2;
    AlertDailog.Builder builder;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Builder=new AlertDialog.Builder(MainActivity.this);

        Add = (Button) findViewById(R.id.bnAdd);
        Subtract = (Button) findViewById(R.id.bnSub);
        Answer = (TextView) findViewById(R.id.TVAns);
        Num1 = (EditText) findViewById(R.id.ETNum1);
        Num2 = (EditText) findViewById(R.id.ETNum2);
        Add.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                num1 = Double.parseDouble(Num1.getText().toString());
                num2 = Double.parseDouble(Num2.getText().toString());

                builder.setTitle("Mycal Alert Dialog");
                builder.setMessage("You are going to add the two number" + num1.toString() + "to" + num2.toString() + ",is it ok");
                builder.setPositiveButton("OK", new DialogInterface.OnCancelListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        Ans = num1 + num2;
                        Answer.setText(Ans.toString());
                    }
                });
                AlertDialog alertDialog=builder.create();
                alertDialog.show();

            }

        });
        Subtract.setOnClickListener((v)-> {
                num1 = Double.parseDouble(Num1.getText().toString());
                num2 = Double.parseDouble(Num2.getText().toString());
                Ans = num1 - num2;
                builder.setTitle("Mycal Alert Dialog");
                builder.setMessage("You are going to Subtract the two number"+num2.toString()+"from"+num1.toString()+"do you want to show the answer on the top? or on a  toast notification");
                builder.setPositiveButton("show on top",new DialogInterface.OnClickListener(){
                builder.setPositiveButton("OK",new DialogInterface.OnCancelListener() {
                                @Override
                                public void onClick(DialogInterface dialog,int which) {
                                   Answer.setText(Ans.toString());
                                }
                            });
                builder.setNegativeButton("show  Toast",new DialogInterface.OnCancelListener() {
                        @Override
                        public void onClick(DialogInterface dialog,int which) {
                           Toast.makeText(MainActivity.this,"your answer is"+AnstoString(), Toast.LENGTH_LONG).show();

                        }
                });
                AlertDialog alertDialog=builder.create();
                alertDialog.show();

        }};

    }
}


