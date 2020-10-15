# lab-22-reading

## What did I learn?
I learned that in the JavaScript code, there is a function called say_hi. It uses the getElementById to locate the DOM element representing the input element with the id first_name. The object returned has a method value that will return the text the user has typed in that field. This technique is used to retrieve the content of both input fields and assign their content to two variables: fname and lname. Then, using these variable it can create an HTML snippet and assign it to a new variable called html. Then it can set the innerHTML attribute as earlier to show the HTML it generated. 

An example of the code would be:

<html>
<head>
  <title>Hello World</title>
</head>
<body>
 
First name: <input id="first_name">
Last name: <input id="last_name">
<button id="say">Say hi!</button>
 
<hr>
<div id="result"></div>
 
<script>
function say_hi() {
    var fname = document.getElementById('first_name').value;
    var lname = document.getElementById('last_name').value;
 
    var html = 'Hello <b>' + fname + '</b> ' + lname;
 
    document.getElementById('result').innerHTML = html;
}
 
document.getElementById('say').addEventListener('click', say_hi);
</script>
 
</body>
</html>
