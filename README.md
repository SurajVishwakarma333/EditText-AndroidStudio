# EditText-AndroidStudio

• Edittext refers to the widget that displays an empty textfield in which a user can enter the required text and this text is further used inside our application.


# .java file


    import androidx.appcompat.app.AppCompatActivity;

    import android.os.Bundle;
    import android.view.View;
    import android.widget.Button;
    import android.widget.EditText;
    import android.widget.Toast;

   public class MainActivity extends AppCompatActivity {

    EditText name, password, email, contact, date;
    Button submit;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        name=findViewById(R.id.editText1);
        password=findViewById(R.id.editText2);
        email=findViewById(R.id.editText3);
        contact=findViewById(R.id.editText5);
        date=findViewById(R.id.editText4);
        submit=findViewById(R.id.btn);


        submit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (name.getText().toString().isEmpty() || password.getText().toString().isEmpty() ||
                    email.getText().toString().isEmpty() || date.getText().toString().isEmpty() ||
                    contact.getText().toString().isEmpty())
                {
                    Toast.makeText(getApplicationContext(), "Enter the Data",Toast.LENGTH_SHORT).show();
                }
                else {
                      Toast.makeText(getApplicationContext(),
                                          "Name - " +  name.getText().toString() +
                                      " \n" + "Password - " + password.getText().toString() +
                                      " \n" + "E-Mail - " + email.getText().toString() +
                                      " \n" + "Date - " + date.getText().toString() +
                                      " \n" + "Contact - " + contact.getText().toString(),
                              Toast.LENGTH_SHORT).show();
                }
            }
        });
        }
      }

# PROJECT OUTPUT :

![editText](https://user-images.githubusercontent.com/101108540/173174124-62dc7c61-96e7-403a-b306-1c45e1969cd0.jpg)

# Attributes of editText :

1. id : id is an attribute used to uniquely identify a text EditText.
   
            android:id="@+id/simpleEditText"

2. text : text attribute is used to set the text in a EditText.
   
            android:text="Username"

3. ems : basically it works on width resizing of editText.
   
            android:ems="20dp"

4. inputType = it is use for what type of editText we want eg-name,phone,date,dateTime,etc
   
            android:inputType="name"
            android:inputType="phone"
            android:inputType="date"

5. gravity: The gravity attribute is an optional attribute which is used to control the alignment of the text like left, right, center, top, bottom, center_vertical, center_horizontal etc.
  
            android:gravity="right"      
![right](https://user-images.githubusercontent.com/101108540/173035203-3e0044c3-835d-44fb-afff-af11c8e9c0f3.jpg)


6. hint: hint is an attribute used to set the hint i.e. what you want user to enter in this edit text. Whenever user start to type in edit text the hint will automatically disappear.
  
            android:hint="Enter Your Name Here"

7. textColor: textColor attribute is used to set the text color of a text edit text. Color value is in the form of “#argb”, “#rgb”, “#rrggbb”, or “#aarrggbb”.
   
            android:textColor="#f00"

8. textColorHint: textColorHint is an attribute used to set the color of displayed hint.
 
            android:textColorHint="#0f0"

9. background: background attribute is used to set the background of a edit text. We can set a color or a drawable in the background of a edit text.
   
            android:background="#000000"
      
 ![background](https://user-images.githubusercontent.com/101108540/173035381-9ea64783-0694-49a9-b009-e9d453d86763.jpg)


10. textStyle: textStyle attribute is used to set the text style of a edit text. The possible text styles are bold, italic and normal. If we need to use two or more styles for a edit text then “|” operator is used for that.
  
            android:textStyle="bold|italic"
