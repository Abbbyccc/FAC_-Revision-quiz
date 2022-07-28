# FAC_Revision-quiz
## Git
#### Why do we use Git?
To control and track our project code. Git tracks the changes you make to files, so you have a record of what has been done, and you can revert to specific versions should you ever need to.

#### What’s the difference between Git and GitHub?
Git is a control system let you manage the project code history, and GitHub is cloud-base hosting service for you let you manage git repos.

#### What happens when you clonea repository?
You clone a full copy of all the repository to your chosen location.

#### What happens when we do git pull origin main
Pull changes from the origin remote, master branch and merge them to the local checked-out branch.

#### How do we create a new branch on our local machine?
Open the terminal in the project directory and enter [ git checkout -b “branch name” ] 

#### How do we control which changes will be included in the next commit?
Use [ git add "the changed file name" ]

#### When might git add .be inappropriate?
With [ git add .], you are adding every single file in the current folder, or structure, or anything else in the directory, you could add generated files, backups, and confgiure files which you proberbly don't want to add.

#### How do we make sure our local changes don’t conflict with main?
Always ceate a branch that separate from the main to work on

#### What does git push origin [branch-name] do?
It will create a Pull Request under the [branch-name]

#### Why do we make pull requests instead of just changing main directly?
To carefully review the code and create different version to track before merge the file into the main

#### Why should you review your teammates’ pull requests?
To double confirm there is no bug and understand other people’s work to 


## HTML
#### Why is accessibility important?
For people with disabilities can access the same things as those without a disability.

#### How can you quickly find simple accessibility problems?
Use lighthouse assessment from Chrome Dev tool

#### What is semantic HTML?
Semantic HTML is a coding style. It is the use of HTML markup to reinforce the semantics or meaning of the content.

#### Why is it important to use the “correct” semantic element?
It helps structure the code we create, making it more readable and easier to maintain.

#### What is the "form" element used for?
<form> represents a document section containing interactive controls for submitting information.


## CSS
#### How would you use CSS variables to make a reusable colour palette?
Define variables with the syntax --var-name: value. Commonly done on :root (= <html>)
for example:
```
:root{
 --theme-main-color:;
 --dark-color:
 --light-color:
}
```
and use the color variable like below

h2{
    color:var(--theme-main-color);
}
#### How would you use flexbox to make elements sit on a single line?

first make sure all elements is under the same container class= "line-container"
```
.line-container { 
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    }
```
#### How would you use grid to make a layout that automatically adds columns as the screen gets wider?
add following syntax to css 
```
grid-container{
    isplay: grid;
    grid-template-columns: repeat(repeat(auto-fill, minmax(100px, 1fr)));;
}
```
#### Why is it important to create a responsive design?
Because nowadays people use all different devices with different sizes to browse the web pages How would you structure your CSS to make it “mobile-first”?

## Javascript
#### Why should we avoid using var to define variables?
They can easily be accessed by outside manipulation

#### How might you make a long, complex chunk of code easier to read?
- Reuse What Will Be Used More Than Once. "Don't repeat yourself"
- Make Modules, Classes, or Components as Small as Possible
- Automate Rules and Guidelines for Your Code
- Write code Like You’re in a Team — Even a One-Person Team

#### What is a “callback”?
A callback function is a function passed into another function as an argument


## Array methods
#### How would you use array.map() to create a new array with transformed values?

```
const array1=[1,2,3,4,5]
const transformed=array1.map(x=>x+1)
console.log(transformed) // [2,3,4,5,6]

```
#### How would you use array.filter() to create a new array with certain values removed?

```
const array1=[1,2,3,4,5]
const filtered=array1.filter(x=>x>3)
console.log(filtered) // [4,5]
```

#### How would you use array.find() to get a single value from an array?

```
const array1 = [5, 12, 8, 130, 44];
const found = array1.find(element => element > 10);
console.log(found); // 12
```

## Promises & fetch
#### What is a promise?
A promise is an object that may produce a single value some time in the future

#### How do promises help manage asynchronous code?
Inside an async function you can use the await keyword before a call to a function that returns a promise. This makes the code wait at that point until the promise is settled, at which point the fulfilled value of the promise is treated as a return value, or the rejected value is thrown.

#### What does a promise’s.then method return?
The then method returns a Promise which allows for method chaining.

#### How could you chain promises together to avoid “callback hell”?
Multiple .then and .catch to catch any error

#### How would you handle a fetch request that failed to get a response from the server?
For HTTP errors we can check the response. ok property to see if the request failed and reject the promise ourselves by calling return Promise.

#### How would you handle a fetch request that received a 404 response from the server?



## HTTP
#### What is an HTTP request?
HTTP request is made by a client, to a named host, which is located on a server.

#### What kind of request is sent when you click a link in your browser?
Your browser takes that URL, breaks out the name of the web site, and then uses the Domain Name System (DNS) to get an Internet Protocol (IP) address for the site.

#### What kind of request is sent when you submit a form in your browser?
'POST' HTTP method

#### What is an HTTP response?
An HTTP response is made by a server to a client. as a status text

#### What does the status code of an HTTP response tell us?
whether a specific HTTP request has been successfully completed

#### What are some common status codes?
```
<ul>
<li>HTTP Status Code 200 - OK.</li>
<li>HTTP Status Code 404 - Not Found.</li>
<li>HTTP Status Code 500 - Internal Server Error.</li>
<li>HTTP Status Code 503 - Service Unavailable.</li>
</ul>
```
#### What are HTTP methods for?
#### What kind of request should have a GET method?
The HTTP GET request method is used to request a resource from the server. T/p>

#### What kind of request should have a POST method?
POST is used to send data to a server to create/update a resource.

#### What kind of request should have a PUT method?
The PUT method requests that the enclosed entity be stored under the supplied URI.

#### What kind of request should have a DELETE method?
request method is used to delete the specified resource

#### What is the “body” of an HTTP request for?
A request body is data sent by the client to your API.
#### What is the “body” of an HTTP response for?

## DOM
#### How would you get a reference to a DOM element in your JS?
use Event.target
#### How would you get references to multiple DOM elements at once in your JS?
#### How would you update properties of a DOM element?
getAttribute() and setAttribute().
#### What’s the difference between a “property” and an “attribute”?
An attribute is the initial state when rendered in the DOM. A property is the current state. In most cases, attributes and properties are kept in-sync automatically.
#### What are some different ways to add content inside a DOM element?
createElemet(). createChildNode
#### When might the [template] element be useful?
#### What are the different ways to add event handlers to elements?
#### Why is addEventListener the safest way to add an event handler?
#### How can you access submitted form values in your JS?
pass in an event handler function into the onSubmit prop to get the inputted form values.

## Testing
#### Why are tests useful?
to test if all functionalities are working as desired.
#### What is the difference between unit and integration tests?
#### What kind of code is easier to test?
#### Why should your tests be isolated from each other?
#### What is Test Driven Development (TDD)?
#### When might TDD be a useful process to follow?

## Debugging
#### What process would you take to find out why your code isn’t working?
#### What tools do JS/dev tools have to help debug your code?
#### At what point should you ask for someone else’s help?
