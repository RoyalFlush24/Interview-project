# Interview-project

## Question 1

#### What is the most influential book or blog post you’ve read regarding web development?


The blog post I’ve read from six revisions about “How Web Design Impacts Content Marketing”. It was really impression because it my as new web developer I never knew how the appearance alone make or break your site. Sometimes when I visit certain sites, and I have a hard time looking for something normally I try other different sites and not return to the sites that game me a challenge. To me I just view it as maybe it doesn’t have what I’m looking for, but it turns out it was because 1) the site was not appealing in appearance, 2) Accessibility to the information I was looking for was extremely difficult which was frustrating. An unorganized website will not give you the result you were hoping for because of the readability of your site. People need to be able to read your site without being confused or without too many different things catching their attention for examples pops like every 3 seconds.


## Question 2

#### Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?


I built an item-catalog web app that allowed us to use either google or Facebook oauth. I chose to built it because it was a requirement to complete the Nanodegree. I learned how to built an app and use both google and Facebook API to log into the application. The challenges I had was to have both APIs working simultaneously together without one interrupting the other which was extremely challenging for me. I was able to get google login to work, but when I log in I can’t successfully log out; so I had to reconfigure my app and by doing that my Facebook login was calling on the google access token to login which was giving me errors. I had some help from some classmates as I’ve exhausted every effort imaginable. Turns out not all my codes under gconnect was under gconnect some were being used as equivalent to the function @app.route(gconnect) which was messing up both my google and Facebook oauth.


## Question 3

#### Write a function that takes a list of strings and returns a single string that is an HTML unordered list `(<ul>...</ul>)` of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?


```python
def print_ul(elements):
    print("<ul>")
    for s in elements:
        ul = "<li>" + str(s) + "</li>"
        print(ul)
    print("<ul>")

fruits = ['strawberry', 'mango', 'banana', 'oranges', 'watermelon', 'grapes', 'blueberries'];
print_ul(fruits)

```


## Question 4

#### List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?

Cookie poisoning/hijacking- is when the attacker modify the valid cookie and gain false authorisation to information about another user and go on to steal your information.
Clearing stored cookies from your browser regularly will ensure that there is nothing for anybody to hijack. Always avoid signing up for sites and or newsletters that you don’t trust or won’t use again.

Brute Force Attact- are used to have access to password-protection sections and contents. Using applications like fail2ban to help protect against these attack by automatically changing or configuring the firewall to deny access from the attacker IP address after a number of failed attempts.

SQL Injection- these are the most serious attacks on the web as it uses web applications vulnerabilities to gain access to databases and all the information contained in that database.
By regularly practicing auditing and remediation of your application you can ensure that any vulnerability found can be dealt with as quickly as possible before someone else has to chance to exploit your application.

## Question 5

#### Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.

```python
from flask import Flask
app = Flask(__name__)

import json
import random


@app.route('/')
def hello_world():
  return 'Hello World!'

# Route takes one argument, the number of sides on the die
@app.route('/roll_dice/<int:sides>/json')
def roll_dice(sides):
  """Return the result of two dice with user-specified number of sides
  being rolled as a json object"""

  # Assign the result of the die roll
  die1 = random.randint(1,sides)
  die2 = random.randint(1,sides)

  # Return the results of the dice rolled as json string, sorted by key
  return json.dumps({'die1': die1, 'die2': die2}, sort_keys=True)

if __name__ == '__main__':
  app.debug = True
  app.run()

```
With the starter code I was given I've added the functionality to roll two dice and return the result as a json string. I've also included inside the function the ability to pass the number of sides the dice have to the function since it wasn't specified and expanded the functionality, and the result of each die roll is assigned to a variable. The function returns the results of json.dumps(), sorted by key.

# Question 6 

#### If you were to start your full-stack developer position today, what would be your goals a year from now? 

My goal a year from now is to gain as much experience as I can to be in a position to where I can mentor someone else especially coming from a different field as it is not easy. I would like to learn as much as I can in building web apps from inside out, perhaps taking other nanodegrees to learn more about front-end and back-end to be a well rounded web developer. If the opportunity present itself I'll also learn other languages such as Node.js, c#, c++, etc. 

Coding has always been a dream for me, and I would like to have my own tech company some day.
