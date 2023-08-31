* Continuous Integration and Continuous Deployment/Delivery is a way to take code, package it up and deploy it to a system. That system could be anything like a VM, an EC2, etc.

## What is CI? ##

* Continuous Integration, in this you take the code and you package it up. Think of it like a gift that you are wrapping. Suppose the gify comes to you in pieces, once you recieve that you put that together. And then you wrap it in a wrapping paper. That's your CI process. You are taking the code, you are packaging it up, and then you give it to the CD process.

* There are a few key pieces of CI.

  1. The first is, you package up that code. Let us say you are in your GitHub, and you have a GitHub repository and that repo has different folders or directories with diffreent pieces of code in it. Inside of your CI process, it does a clone of that GitHub repository, and then it packages it up.
  2. The next in CI process is where we test our code, like unit tests would run automatically, integration tests, etc. You want to make sure that code is ready to go. Before you even try to deploy it, you want to make sure it passes all your tests, it has all of the dependencies that are needed.
  3. The last thing is you would typically run any type of security checks against the code.


