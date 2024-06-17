# Asynchronous JavaScript And XML

[_These notes are from W3schools.com_](https://www.w3schools.com/xml/ajax_intro.asp)

<br>

AJAX is a technique for accessing web servers from a web page.

It allows you to:

* Read data from a web server after a page has loaded
* Update a web page without reloading the page
* Send data to a web server in the background

Since AJAX allows webpages to be updated asynchronously by exchanging data with a web server behind the scenes, it is possible to update parts of a web page without reloading the whole page.

<br>

It uses a combination of:

* a browser built-in XMLHttpRequest object (to request data from a web server)
* JavaScript and the HTML DOM (to display or use the data)

Note:  Modern Browsers can use Fetch API (whose interface allows web browser to make HTTP requests to web servers) instead of the XMLHttpRequest Object.

<br>

Sequence of events within AJAX:

1. An event occurs in a web page (for example: the page is loaded, a button is clicked, etc.)
2. An XMLHttpRequest object is created by JavaScript
3. The XMLHttpRequest object sends a request to a web server
4. The server processes the request
5. The server sends a response back to the web page
6. The response is read by JavaScript
7. Proper action (like page update) is performed by JavaScript

<hr>

<hr>

## 1. Create an XMLHttpRequest Object

All modern browsers (Chrome, Firefox, IE, Edge, Safari, Opera) support/have a built-in XMLHttpRequest object.

The XMLHttpRequest object can be used to exchange data with a web server behind the scenes. This means that it is possible to update parts of a web page without reloading the whole page.

Syntax for creating an XMLHttpRequest object:

        variable = new XMLHttpRequest();

## 2. Define a Callback Function

A callback function is a function passed as a parameter to another function.

In this case, the callback function should contain the code to execute when the response is ready.

        xhttp.onload = function() {
          // What to do when the response is ready goes here
        }

## 3. Open the XMLHttpRequest object

Use the `open()` method of the XMLHttpRequest object.

        xhttp.open("GET", "ajax_info.txt");

For security reasons, modern browsers do not allow access across domains.  This means that both the web page and the XML file it tries to load, must be located on the same server.

## 4. Send a Request to the Server

To send a request to a server, use the `send()` method of the XMLHttpRequest object:

        xhttp.send();
