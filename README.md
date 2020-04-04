Some notes on this exercise:
This exercise approaches get and post. Below are some notes from TA regarding this exercise from March 2020.

Differences between GET and POST:
GET, is called safe method because no matter how many times you use it, GET will never change any information on the server. It is only a request for information. Since we are switching from asking the server for information to working with sessions, we are going to do something different. Our first request for a survey is going to set our session survey list to an empty list. This is a change. It's not the server, per se, but it is not the web page: we are having the web page change something else. This is why we are now using a POST. We may not be sending any information, but we are initiating change, and that's one of the biggest differences between GET and POST.

Things to do before this exercise:

I would just try to inspect and analyze all the attributes that the Survey class has defined (in its __init__ function), as well as the Question class. So, when the satisfaction_survey is created as an instance of the Survey class, we pass arguments like title, instructions and a list of questions.

Initially, you can run ipython and then the %run surveys.py command to execute the code and gain access to the classes and object instances created inside of it.

You can first just enter satisfaction_survey in the command line and you should get a return which identifies that it's created from the Survey class an the memory address location - which indicates that it's defined. Then, based on what you see in the Survey __init__ function, you can start analyzing the instance attributes that the satisfaction_survey object has present.

You can type satisfaction_survey.title and satisfaction_survey.instructions to see the string values passed to those fields. Then, you can enter satisfaction_survey.questions and you should see a list of Question class instances for that particular survey instance.

To create each particular question instance, we call the Question class and provide the question string as an argument, as you can see in the surveys.py code where satisfaction_survey is defined.

Going from there, you can use index numbers to access each Question instance object individually, e.g. satisfaction_survey.questions[0]

Then, you can check the Question class __init__ method and see the attributes that each question instance should have, and test those in the command line, for example:
satisfaction_survey.questions[0].question
satisfaction_survey.questions[0].choices
satisfaction_survey.questions[0].allow_text

Then, you can analyze those fields for different questions by changing the [0] index number to access a different question from the satisfaction_survey.questions list.




