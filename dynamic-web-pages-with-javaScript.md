## .html files
Web developers usually talk about three languages that are used to create web pages: HTML, CSS, and JavaScript.

## .css files
Where possible, aim to keep the three languages in separate files, with the HTML page linking to CSS and JavaScript files.

## .js files
Each language forms a separate *layer* with a different purpose. Each layer, from left to right. builds on the previous one.

> JavaScript is written in plain text, just like HTML and CSS, so you do not need any new tools to write a script. This example adds a greeting into an HTML page. The greeting changes depending on the time of day.

### SUMMARY
#### How do I write a script for a web page?
1. It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files (like HTML pages and CSS style sheets), but they have the . j s extension.
1. The HTML <script> element is used in HTML pages to tell the browser to load the JavaScript file (rather like the <link> element can be used to load a CSS file).
1. If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.
  

#### A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a *statement*. Statements should end with a semicolon.
- **JAVASCRIPT IS CASE SENSITIVE** JavaScript is case sensitive so hourNow means something different to HourNow or HOURNOW.

####  You should write *comments* to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.
- MULTI-LINE COMMENTS
- SINGLE-LINE COMMENTS

#### A script will have to temporarily store the bits of information it needs to do its job. It can store this data in *variables*. A variable is a good name for this concept because the data stored in a variable can change (or vary) each time a script runs.
- Remember the value for **width**
- Remember the value for **height**
- Multiply width by **height** to get the area
- Return the result to the user

### DATA TYPES
- NUMERIC DATA TYPE
  - `0.75`
- STRING DATA TYPE
  - `'Hi, Ivy!'`
- BOOLEAN DATA TYPE
  - `true`
  
###  RULES FOR NAMING VARIABLES
1. The name must begin with a letter, dollar sign ($),or an underscore (_). It must not start with a number.
1. The name can contain letters, numbers, dollar sign ($), or an underscore (_). Note that you must not use a dash(-) or a period (.) in a variable name.
1. You cannot use *keywords* or *reserved* words. Keywords are special words that tell the interpreter to do something. For example, var is a keyword used to declare a variable. Reserved words are ones that may be used in a future version of JavaScript.
1. All variables are case sensitive, so score and Score would be different variable names, but it is bad practice to create two variables that have the same name using different cases.
1. Use a name that describes the kind of information that the variable stores. For example, fi rstName might be used to store a person's `firstname` for their last name, and age for their age.
1. If your variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word. For example, `firstname` rather than `firstname` (this is referred to as camel case). You can also use an underscore between each word (you cannot use a dash).
