# wordCounter

I used Jetbrains IntelliJ / Java for my IDE / language.
I zipped the project, built an executable jar, and uploaded both to this repo.
In order to run the project, download the jar and run it.
(when you're finished, don't forget to go to the task manager and end the "Java(TM) Platform SE binary" background process)

Open a browser and go to localhost:8080/counter

I have the values defaulted to id=1&message=demo if you don't specify in the URI.

If you want to be more specific, use localhost:8080/counter?id=*int*&message=*string*

Due to the hustle/bustle of thanksgiving/black friday, I didn't get a chance to start on this until late Tuesday night 
and spent more time creating a github account/uploading the project than actually doing the project.


Next day update: I just realized I didn't use JSON...and the challenge specifically requested JSON - I got wrapped up around the logic of the challenge, using in-browser testing while I got it working...then I forgot to go back and use JSON.

If I were to implement JSON input/output, I would create a request POJO containing ID and Message and a response POJO containing Counter...then use them in my controller by accepting the request object as input and returning the response object instead of a string. I would also specify @RequestMethod=POST on the input. I would also change the testing method to use postman instead of in-browser testing.

Coding Challenge for Software Engineer Applicants:
1. Create a REST service with a single endpoint that accepts a json message with two fields.."id" and "message". (example: { "id": "123", "message": "hello world" })
2. The endpoint should return a json document with a single field "count" that contains the total number of words contained in all the messages received to that point.
For example, if the first message contains 3 words it would responsd with count = 3. If the next message contains 5 words it would respond with count = 8.
3. The service should ignore messages with duplicate ids. (i.e. ids that have already been processed)
4. Use the programming language of your choice.
5. Upload all code to a public github repo with a readme that explains how to build and run the project
