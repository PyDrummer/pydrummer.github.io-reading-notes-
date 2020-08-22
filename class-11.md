# Images

Important take aways from this chapter:

You can control sizes of images with CSS with the width and height properties.

Aligning images with CSS is possible by using float: left or right then controlling the margin amount.

By using display: block; and margin auto you can easily center images.

#### Background

Background images can be added in CSS with background-image: url("link goes here");

More on page 415

# Practical Information

#### Search Engine Optimizatrion

SEO is the practive of helping your site appear nearer the top of search engine results.

Search engines dont just look at whats on the site, they also consider how many sites link to yours. So they consider both on page and off page aspects.

On-page techniques: Keywords within the HTML code that people are likely to enter to a search engine if they want to find your site.

Off-page techniques: Getting other sites to link to your page, search engines also look at the words between the opening <a\> tags.

On-page SEOs can include the page title, url address, headings and much more.

Next you must decide which keywords and phrases to add to your site to gain visability. 

#### Utilize google analytics

Once your site is live use www.google.com/anlytics to see how someone found your site and how many people used your site.

# Chapter 9 JS book

```
var liEls = document.getElementsByTagName('li');

if (elements.length > 0) {
  var el = liEls[0]
  el.className = 'cool';
}
```

the code above looks for any <li\> in the document. It stores the result into a var. The if statement checks if any of the li's were found. if matching elements were found the first one is selected and it's class attribute is updated to 'cool'.

Node lists can be created by finding multiple elements. When you do have a Node list you can iterate through it with a for loop. Simply use the Node list's lenght while iterating.

Here is a quick example of how to create a node list:
```
var nodeList = document.querySelectorAll('li.cool');

for (var i = 0; i < nodeList.length; i++) {
  nodeList[i].className = 'hot';
};
```
We just grabbed all the list items with a class of cool, stored them in an array of nodeList. Next we iterated through the length of nodeList array and changed each nodeList item's class name to 'hot'.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
