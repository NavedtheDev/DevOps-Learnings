## Class ##
* A class is like an object constructor.
* All classes have a __ init __() function.
* __ init __() is executed automaticaly whenever we create the objects from this class.
* This __ init() __ is constructor in python. This will help us construct objects from that user class.



```
class User:
    def __init__(self, e, n, p, cjt):
        self.email = e
        self.name = n
        self.password = p
        self.current_job_title = cjt

    def change_password(self, new_p):
        self.password = new_p

    def change_job_title(self, new_jt):
        self.current_job_title = new_jt
```

* <b>self</b> parameter is a reference to the current instance of the class. It is used to access variables that belong to that class.
