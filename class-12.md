# Chart.js

I decided to combine the reading material and make a quick tutorial

First you'll need to download chart.js with either npm or by downloading the files directly from their github. Once downloaded bring the chart.min.js file into your directory. Later we will call that file with a <script\> tag.

An alternate method is to grab the chart.js CDN and link it into your HTML

Now that you have chart.js lets code.

```
// Within the head element of your HTML add this:
<script src='Chart.min.js'></script> // to grab the chart.min.js source in your directory

// Now we will add a canvas element and set an id, width and height.

<canvas id="example" width="500" height="500"></canvas>
// By using width and height you can alter what the graph dimensions will look like.

// Next write your script to retrieve the context of the canvas. Make sure to create a varible to assign the location your graph will go with document.getElementById('example').getContext('2d');
// After that you'll need a new Chart(example).Line(exampleData); we will add the exampleData var next.
                                               ^ Notice the word line is indicating we are creating a line graph.

// Now we write the data within the same script.

var exampleData = {
  labels : ["Example1","Example2","Example3"]
  datasets : [
    {
      fillColor: "rgb(1, 100, 300)",
      data : [203,156,99,251,305,247]
    }
  ]
}
```

This was a quick example of a line graph sources used: https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/

Pie charts are similar but in the exampleData area you would have {curly brackets} around the values and colors to signal how much of the pie chart each color will take up. Then you add the pie chart options in a new variable.

There are many other types of charts you can make depending on the type of data you would like to show.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
