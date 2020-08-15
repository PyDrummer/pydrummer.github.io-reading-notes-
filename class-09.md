# HTLM Forms

Let's learn how to create forms! The best known form on the web is probably the search box that sits right in the middle of Google's homepage.

We can create text forms for usernames and passwords, a multiline text area, radio buttons, checkboxes, and drop-down boxex.

Other options include buttons to submit data from the form to another webpage and a way to upload files.

You can combined two of these options together while makings forms.

<form\> is how you call this element, you give it an action as a url that will receive the information and a method.

#### Form method

- get the values from the form are added to the end of the URL specified in the action attribute.
- post, the values are sent in what are known as HTTP headers.

Post is generally used when users upload a file, if it contain sensitive data, and if it adds or deletes info from a database.

after <form\> you will need <input\> which will require a type, name, size and maxlength(used to limit the amount of characters a user may enter into the text field). 

Type can be use for regular text entry or be used as password entry. When it is in the password mode the text is all blocked out.

By using the different types of forms above you can collect information from your user to store and be used later.

input types to note: type = email/url/date/search can be used to add functionality to your website.

# CSS Lists, Tables & Form

There are many list-style-type options with CSS to make your web page look good. Refer to page 333 for multiple options.

Tables can be manipulated with CSS just like any other HTML. By using width and padding you can set the spaces between your items in the tables.

Also you can set a boarder around empty columns making them look filled in.

The main take away from this chapter are recommendations for style choices when using lists, tables and forms.

# JS Events

JS can allow you to create certain events on your web page based on the user's actions. Make the code respond to what the user does.

By utilizing the events from page 246 you can make them trigger events in your script.

I like the book's example of the checkUserName() function event. It will make the script check if the username entered is less than 5 characters and then which actions the JS will take next.

Event handlers look like this:

```
element.onevent = functionName;

```
first select the element, tell the code which event this is bound to then the function's name and code that it will run. Notice there are no parameters on the function name.

Now write your function.
 
