# Login-Signup-MVVM
Welcome friends, I’m Abdo Essam Software Engineer now we will talk about MVVM and implement it in Android Development using Kotlin 

Creating an app is very easy, but writing a structured code, that is maintainable for the long term and is also testable is not easy.
To write a code that is maintainable, understandable and testable, we follow design patterns.
So here in this repo, I am with you to teach you all how to follow the most popular design pattern that is used to develop android applications.
And yes, I am talking about the MVVM, or Model View View Model design pattern.
This pattern is also recommended and loved by google.
Before moving onto the MVVM, let's first discuss something about design patterns in general.
Like why we need a design pattern.
We were developing the apps and it was working well, now what is the need to make things more complicated.
But when we talk about an app, most of the times it is a product.
So, assume this scenario you were working on an app in a company.
It was working well, but after some time you left the company and a different person came to work on the same application.
This person now will face a lot of difficulty to understand what you have written.
Reading a badly written code by someone else is nothing less than a nightmare.
But if we follow proper guidelines, design patterns and the best practices to write code,
it is easy to understand for anyone.
So, the point number one of using Design Pattern is to make our code more understandable.
If the code is understandable then it is easy for any developer to start working on it and
even for you (if you are the original author of the code).
And you know this very well if you touch your project that you written like 3,4 months before then you yourself face difficulties understanding it.
So, following a proper design pattern makes our project maintainable for a long run.
You know as a beginner how we create apps while learning.
We put everything in our activity or fragment classes.
Like a network call, and all the other heavy things, everything we put inside the activity or fragment classes.
And you know this is the worse practice of writing code.
This makes our codes tightly coupled that means more dependent on each other.
And if you are from a computer science background you may have learned that tightly coupled software codes are very bad.
But when we follow a design pattern, we take care of coupling and it makes our project
loosely coupled.
And if our project is loosely coupled, it is easy to test so following a good design
pattern makes our project testable as well.
And if our project has all these things that we just discussed it is easy for us to make
changes on the existing project and add new features.
I guess now you understand very well that why using a design pattern is necessary for
building a good application.
Google suggest some common architectural principles that almost all the design pattern follows.

The first thing is separation of concern.
As we discussed we write all the codes in activity or fragment this is the most common mistake.
Our activity or fragment should contain the logics that are responsible for UI related things only.
One of the common problems you might have already faced, when we use retrofit in our fragment and try to update the UI by fetching some data our application crashes.
The problem is we don't own the Fragment, or Activity and the android system can destroy
it anytime because of the android system needs for example in case low memory.
So, if we are trying to update a fragment that is already destroyed, it leads to the crash.
So, we should make these UI classes independent from our network calls.
And doing this we can avoid the lifecycle related problems.
The next principle is we should derive the UI data from a model.
Model is the component that is responsible for handling data of the application and it is independent from the views.
And because it is independent from the views it is unaffected by the lifecycle problems.
Now the main question is why you should use MVVM?
We have the other design patterns as well like MVC, MVP then why MVVM?
The selection of a pattern completely depends on your need.
There is no perfect pattern exist that solves all the problem.
Every pattern has their own advantages and disadvantages, and according to the problem they are chosen.
Google recommends using MVVM.
Actually, the term MVVM is never openly said by google.
But the pattern it is recommending is popular as MVVM in the developer community.
Google says we should use it, but it also says that if we have some other pattern that is
following the common architectural principles then you can keep using it.
This diagram explains the MVVM architecture.
 
<div align="center">
  <img src="https://files.codingninjas.in/article_images/android-mvvm-model-view-viewmodel-architecture-0-1647677770.jpg" width="600" height="300"/>
</div>

First, we have the Activity or Fragment classes, and it is basically the UI of our application.
To display data, we will use the Data Binding with the help of View Model.
So, our activity is just dependent on View Model to get the data.
Now the benefit is View Model will not update the data if the view is destroyed so the problem of lifecycle changes is solved.
View Model will fetch the data from the repository, so again View Model is just dependent on the repository to get the data.
The repository may use the local database that is SQLite or our backend server using Restful API.
So only repository is dependent on multiple data sources to get the data.
In this approach we use local first, that means we will try to fetch the data from local storage first, because if the user has a connectivity issue application will still work.
Because using RESTful API for the data requires network connection to be available.
As you can see the architecture is separating everything.
But while coding you may end up thinking that hey why I cannot directly get the data from SQLite instead of following this View Model and Repository chain.
But trust me it is very important, so keep in mind you always follow this rule and never
skip anything.
So that is all for this repo friends.
I hope you are excited about this article.
So let me know your excitement by staring it.
thanks for you guys.

