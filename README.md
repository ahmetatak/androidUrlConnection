
# HttpAsyncTask
Android URL Connection helps you to send and get data to an url in android
Connect to url and send post via HttpAsyncTask.java  in android !


![alt text](https://user-images.githubusercontent.com/3717312/28491871-d49c365a-6f00-11e7-8350-3a7141c9ef90.png)

## Getting Started

the class will help you to connect an url (request-response) in android. it returns the data in string format.
#### YourActivity

import HttpAsyncTask.java class to your project.
open your activity forexample; if you are going to use it in your onCreate() method;
```
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_message);
                HttpAsyncTask task = new HttpAsyncTask();//initialization
                HashMap<String,String> post = new HashMap<String, String>(); //we will send the post in HashMap
                post.put("username","ahmet");// post  name,value if you do not want to use it you can just leave empty
                post.put("password","ca22ff0def0e2e0a320e351fc3060998");
                String url ="http://mywebsite.com/login.php";//your url

                String data = task.start(getApplicationContext(),post,url);//it will return the result! now we can use it!
                Toast.makeText(getApplicationContext(), "return :"+data,Toast.LENGTH_SHORT).show();// display the result !
        }
```
