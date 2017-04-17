tablesorter
===========

### Flexible client-side table sorting
#### Getting started

To use the tablesorter plugin, include the jQuery library and the tablesorter plugin inside the head-tag of your HTML document:

```html
<script type="text/javascript" src="/path/to/jquery-latest.js"></script> 
<script type="text/javascript" src="/path/to/jquery.tablesorter.js"></script> 
```

Tablesorter works on all standard HTML tables. You must include THEAD and TBODY tags:

```html
<table id="myTable" class="tablesorter"> 
<thead> 
<tr> 
    <th>Last Name</th> 
    <th>First Name</th> 
    <th>Email</th> 
    <th>Due</th> 
    <th>Web Site</th> 
</tr> 
</thead> 
<tbody> 
<tr> 
    <td>Smith</td> 
    <td>John</td> 
    <td>jsmith@gmail.com</td> 
    <td>$50.00</td> 
    <td>http://www.jsmith.com</td> 
</tr> 
<tr> 
    <td>Bach</td> 
    <td>Frank</td> 
    <td>fbach@yahoo.com</td> 
    <td>$50.00</td> 
    <td>http://www.frank.com</td> 
</tr> 
<tr> 
    <td>Doe</td> 
    <td>Jason</td> 
    <td>jdoe@hotmail.com</td> 
    <td>$100.00</td> 
    <td>http://www.jdoe.com</td> 
</tr> 
<tr> 
    <td>Conway</td> 
    <td>Tim</td> 
    <td>tconway@earthlink.net</td> 
    <td>$50.00</td> 
    <td>http://www.timconway.com</td> 
</tr> 
</tbody> 
</table> 
```

Start by telling tablesorter to sort your table when the document is loaded:

```javascript
$(document).ready(function() 
    { 
        $("#myTable").tablesorter(); 
    } 
); 
```

Click on the headers and you'll see that your table is now sortable! You can also pass in configuration options when you initialize the table. This tells tablesorter to sort on the first and second column in ascending order.

```javascript
$(document).ready(function() 
    { 
        $("#myTable").tablesorter( {sortList: [[0,0], [1,0]]} ); 
    } 
); 
```

For DateTime columns you can specify your format, like this:

```javascript
$(document).ready(function() 
    { 
        $("#myTable").tablesorter( {dateFormat: 'pt'} ); 
    } 
); 
```

The available ones (currently) are: us, pt and uk. (for pt you can use 'dd/MM/yyyy hh:mm:ss')
