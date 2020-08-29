# Local Storage

This will be a summary of the Local Storage reading material

It first talks of the past and how storage was handled before HTML5.

The material also speaks about how cookies have flaws such as being limited to about 4 KB of data which isn't that useful.

### History

First Microsoft invented a thing called userData which allowed web pages to store up to 64 KB of data per domain.

In 2002 Adobe made a feature Flash 6 which had a feature known as Local Shared Objects. This could store up to 100 KB of data per domain.

2007 Google made Gears, which provides an API (application programming interface) which allows two applications to talk to each other. The google API goes to an embedded SQL database.

* SQL stands for Structured Query Language, used for managing data held in a relational database management system (RDBMS).

Gears only needed to get permission from the user once, then it could store unlimited amounts of data per domain in SQL database tables.

https://docs.microsoft.com/en-us/sql/relational-databases/tables/tables?view=sql-server-ver15 more about SQL database tables at that link.

Eventually you will find all these solutions are either specific to one browser or reliant on a third-party plugin.

"HTML5 solves this problem with a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins." - from the article (http://diveinto.html5doctor.com/storage.html)

### HTML5 Storage

Specified as Web Storage. Certain browers refer to it as local storage or DOM storage. 

HTML5 Storage is a way for web pages to store named ***key/value*** pairs locally within the client web browser.

Important to know this data being stored is never transmitted to the remote web server. 

#### How JavaScript accesses HTML5 storage.

You must use **localStorage** object in the global **window** object

```
// How to check for HTML5 Storage:
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}

or

if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```

Remember that this data is based on key/value pairs. Keys must be strings, the data can be any type supported by JS. (strings, booleans, ints, floats) regardless of this the data is stored as a string.

#### When you retrieve data and it's a number you will need to use parseInt() or parseFloat()!!

"Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception."

localStorage is an object within JavaScript and can be treated as an associative array. Here is an example from the web page:

```
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);

…could be rewritten to use square bracket syntax instead:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;

-------------------------------------------------------------

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
If you call key() with an index that is not between 0–(length-1), the function will return null.
```

If you need to remove data from a localStorage you must use removeItem() to delete a key and clear() to remove the value.

#### Use an event listener to see when storage is activated

```
if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};

function handle_storage(e) {
  if (!e) { e = window.event; }
}
```
Something important to note is the storage event is not cancelable. There is no way to stop the change from occurring.

Here is a great example of saving a game (link here: http://diveinto.html5doctor.com/canvas.html#halma) on the storage:

```
function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}
```
It's using the localStorage object to save if there is a game in progress. Uses a "gameInProgress" boolean. Then the web page will call a resumeGame() function instead of newGame(). 

the resumeGame checks to see if there was a game in progress after the last localStorage save.

```
function resumeGame() {
    if (!supportsLocalStorage()) { return false; }
    gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
    if (!gGameInProgress) { return false; }
    gPieces = new Array(kNumPieces);
    for (var i = 0; i < kNumPieces; i++) {
	var row = parseInt(localStorage["halma.piece." + i + ".row"]);
	var column = parseInt(localStorage["halma.piece." + i + ".column"]);
	gPieces[i] = new Cell(row, column);
    }
    gNumPieces = kNumPieces;
    gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
    gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
    gMoveCount = parseInt(localStorage["halma.movecount"]);
    drawBoard();
    return true;
}
```
#### Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. 

The end of the article talks about different types of SQLs:

"Oracle’s SQL, Microsoft’s SQL, MySQL’s SQL, PostgreSQL’s SQL, and SQLite’s SQL."

#### An Object Store

The Indexed Database API https://w3c.github.io/IndexedDB/

This is an object store that shares many concepts with a SQL database. The primary difference is that the object store has no structured query language.

You must use methoda provided by the object store to open a *cursor* on the database and enumerate through the records. 

https://hacks.mozilla.org/2010/06/comparing-indexeddb-and-webdatabase/ <link to a walk through for the above.


