# TDD with Python and Django

## This Repo was created for add notes and things abou my Tdd learn
### I'm doing it with the book [TDD with python from Harry J.W. Percival](https://www.oreilly.com/library/view/test-driven-development-with/9781449365141/)

The book have a lot of informations about TDD and start the chapter, installing Django and Selenium, assuming that you have a python running in your machine with a virtual environment activated.

Than, we will install the Django, and Selenium with the commands 

~~~
pip install django

pip install selenium 
~~~

For we do simple things with Selenium, normally the easy way to do it, its use a local webdriver. 

So, we will use for this examples, the Firefox geckodriver. 

[Download here](https://github.com/mozilla/geckodriver/releases/), and set the file in your's environment variable, normally, exist more than one way to set a enviroment variable in your S.O.

One way to do it in linux, its copy the file to **~/.local/bin, something like this:

~~~
cp geckodriver ~/.local/bin/
~~~

After you will be able to run

~~~
geckodriver --version 
~~~

from your terminal, and received something like this: 
~~~
geckodriver 0.26.0 (e9783a644016 2019-10-10 13:38 +0000)

The source code of this program is available from
testing/geckodriver in https://hg.mozilla.org/mozilla-central.

This program is subject to the terms of the Mozilla Public License 2.0.
You can obtain a copy of the license at https://mozilla.org/MPL/2.0/.
~~~


## Notes

#### Functional Tests

* Functional test == Acceptance test == End-to-End test == FTs

* Functional test it's a test that normally check the user side, like if webpage open, and propably will describe how a user story interact with your application, and how this application will answer this user action

* FTs need to have a history readble by a human. We can write this history before the code or/and togheter the code. We can share this comments with a non technical person, i mean with persons not developers, from business side and other's

#### First functional_test_.py example

~~~
from selenium import webdriver

browser = webdriver.Firefox()

#Edith want knows about a new online application,
#this application its a To-Do-List
#She decide to check your Home page

browser.get('http://127.0.0.1:8000')

#She check the title header in page contains Tasks To-Do

assert 'To-Do' in browser.title

#She is invited to insert a task item



#She type "Buy peacock feathers" (pt-br: Comprar penas de pavão) in a text box
#your hobby is fishing, and the feathers is to do bait fishing ( pt-br: isca de peixe)




#When she press enter. the page refresh, and now the page list:
#" 1 - Buy peackok feathers" like a item from list



#Edith it's thinking now if the site will remember yout inputed item, after he leave 
#the page and return again. She saw that application generate a unique url 
#Have a little text about this



#She access the URL and check, your list still in the website



#She like this, and back to sleep

browser.quit()
~~~















