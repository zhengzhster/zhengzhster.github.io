---
layout: page
title: project 3
description: Preparing
img: assets/img/7.jpg
importance: 3
category: work
---

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

<html>
<head>
  	<title>Person Information</title>
  	<meta charset="UTF-8">	<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.19/css/jquery.dataTables.min.css">
	<script type="text/javascript" language="javascript" src="https://code.jquery.com/jquery-3.3.1.js"></script>
	<script type="text/javascript" language="javascript" src="https://cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
</head>

<body>
  <h1>Zheng Zhao</h1>
  <p>Welcome to the MKIs!</p>
  <img src="https://content.codecademy.com/articles/github-pages-via-web-app/happy-ice-cream.gif" />

   <script>
     $(document).ready(function(){
	   var baseurl = "https://jsonplaceholder.typicode.com/todos";
    	 var xmlhttp = new XMLHttpRequest();
    	 xmlhttp.open("GET",baseurl,true);
    	 xmlhttp.onreadystatechange = function(){
    		 if(xmlhttp.readyState==4 && xmlhttp.status ==200){
    			 var persons = JSON.parse(xmlhttp.responseText);
    			 $("#example").DataTable({
    				data:persons,
    				"columns":[
    					{data: "userId"},
    					{data: "id"},
    					{data: "title"},
    					{data: "completed"}
    				]
    			 });
    		 }
    	 };
	 xmlhttp.send();
      });
    </script>


   <table id="example" class="display" style="width:100%">
    <thead>
	    <tr>
	      <th>UserID</th>
	      <th>ID</th>
	      <th>Title</th>
	      <th>Completed</th>
	    </tr>
    </thead>
    <tfoot>
	    <tr>
	      <th>UserID</th>
	      <th>ID</th>
	      <th>Title</th>
	      <th>Completed</th>
	    </tr>
    </tfoot>
    </table>
  </body>
</html>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
