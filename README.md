# Django example

This example is based on [the official Django tutorial](https://docs.djangoproject.com/en/2.2/intro/tutorial01/).

## Prerequisites

* [A python3 virtualenv with python > 3.7](https://code.visualstudio.com/docs/python/tutorial-django)
* [Django is installed](https://docs.djangoproject.com/en/2.2/intro/install/)

## Run unit tests

```bash
$ cd mysite/
$ python manage.py test polls

Creating test database for alias 'default'...
System check identified no issues (0 silenced).
F
======================================================================
FAIL: test_was_published_recently_with_future_question (polls.tests.QuestionModelTests)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/Users/thomas/Dev/Tests/django-example/mysite/polls/tests.py", line 18, in test_was_published_recently_with_future_question
    self.assertIs(future_question.was_published_recently(), False)
AssertionError: True is not False

----------------------------------------------------------------------
Ran 1 test in 0.001s

FAILED (failures=1)
Destroying test database for alias 'default'...
```

To learn more about Django testing visit: [](https://docs.djangoproject.com/en/2.2/intro/tutorial05/)

## Run the web app

```bash
$ cd mysite/
$ python manage.py runserver

Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
May 01, 2019 - 00:15:30
Django version 2.2, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

And visit:

* *[](http://127.0.0.1:8000/polls)*
* *[](http://127.0.0.1:8000/admin)*