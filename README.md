# pyBuilder
####What Is It?####
pyBuilder is an HTML complier, allowing you to dynamically include multiple files (templates) within an HTML document. Because pyBuilder statcially complies the HTML documents after running, any inclusions can be used (.html, .js, .php, etc.).

####How It Works####
pyBuilder parses a file at build time to look for file dependencies, noted in the file by using
```
  <include file="path/to/file[.html][.js][.php]"></include>
```
At this time, pyBuilder reads and inserts the dependent file into the parent file, building an entirely new file (with the same name) inside a newly created build/ directory.

####How To Use It####
1) Add pyBuilder.py to your project directory
<br>
2) run:
```python3 pyBuilder.py path/to/file```
<br>
or
<br>
```python3 pyBuilder.py *```
To build files, use a relative file path (from where the pyBuilder.py file is located) or denote * for all .html files in pyBuilder's current directory (seen in above code snippets).

<br>
*Note: We recommend placing pyBuilder at the beginning of your directory (with your main HTML files), as the ```<include>``` tags currently read file location relative to the builder's location within your directory structure.

####Bugs/Requests####
Feel free to report any issues or feature requests you may have!
