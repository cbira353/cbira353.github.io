---
layout: post
title: "How to Build a Simple Flask application"
excerpt: "We create a simple demonstration of Flask and how we use its simple routing functions to display some quotes on a browser."
categories: articles
tags: [api, python, flask]
author: mbi
comments: false
share: false
modified: 2017-9-07
image:
  feature: church.jpg
  credit: CBIra
  creditlink: http://cbira353.github.io/
---

# 01 How to Build a Simple Flask application
Today we create a simple demonstration of Flask and how we use its simple routing functions to display some quotes on a browser. 

## Setting up the environment
. Make sure you have set up a virtual environment
. Add flask to this environment
`conda create --name FlaskSimple  flask`

Then activate the virtual environment:
`source activate FlaskSimple`

. Make a directory called 'app' and under that another directory, `quotes`
`mkdir app`  and `cd app` , `mkdir quotes`


## Setting up File Structure
. move to the app directory
`cd app`
. create two files and call them app.py and quotes.py
`touch app.py`
`touch quotes.py`

## Setting up the data
. move to the `quotes` directory
. create a file  called `quotes.py` and start a simple dictionary:
```
def funny_quotes():
    return [{
        'author': 'author1',
        'quote': 'Hi'
            },

        {
        'author': 'author2',
        'quote': 'Ho'
        },

        {
        'author': 'author3',
        'quote':'Hee'
        },

        {
        'author': 'author4',
        'quote': 'Heh'
        }
    ]
```

## Setting  up the Flask app
`cd ..` will get you one level up from the quotes directory
. open up the `app.py` file with your basic editor
. create the following code:
```
from flask import Flask, jsonify
import random
from quotes import funny_quotes

app = Flask(__name__)


@app.route("/")
def serve_funny_quote():
    quotes = funny_quotes()
    nr_of_quotes = len(quotes)
    selected_quote = quotes[random.randint(0, nr_of_quotes - 1) ]
    return jsonify(selected_quote)

if __name__ == "__main__":
    app.run(debug=True)

```

## Viewing the Flask app results
. For the most part you are done making the simple Flask app.
. Now it's necessary to start up the app and view its results on the browser:
`python app.py` will get you this result on your terminal:
```
127.0.0.1 - - [06/Sep/2017 15:33:28] "GET /?__debugger__=yes&cmd=resource&f=console.png HTTP/1.1" 200 -
 * Detected change in '/home/mbira/Dropbox/Projects/33FlaskSimple/app.py', reloading
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 174-255-069
127.0.0.1 - - [06/Sep/2017 15:34:13] "GET / HTTP/1.1" 200 -

```

Go to your browser and you will see the random choice of quotes from the quotes.py file:

```
// 20170906153440
// http://127.0.0.1:5000/

{
  "author": "author3",
  "quote": "Hee"
}
```

And that's it. A simple Flask app routed to your browser.
