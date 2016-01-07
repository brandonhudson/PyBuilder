# pyBuilder
####What Is It?####
pyBuilder is an HTML complier, allowing you to dynamically include multiple files (templates) within an HTML document. Because pyBuilder statcially complies the HTML documents after running, any inclusions can be used (.html, .js, .php, etc.).

####How It Works####
pyBuilder parses a file at build time to look for file dependencies, noted in the file by using
<code>
  <include file="path/to/file[.html][.js][.php]"></include>
</code>
At this time, pyBuilder reads and inserts the dependent file into the parent file, building an entirely new file (with the same name) inside a newly created build/ directory.

####How To Use It####
1) Add pyBuilder.py to your directory
2) run:
<code> python3 pyBuilder.py </code>
3)Use a relative file path (from where the pyBuilder.py file is located) or denote * for all .html files in the builder's current directory

*Note: We recommend placing pyBuilder at the beginning of your directory, as the <include> tags read file location relative to the builder's location within your directory structure.

####Bugs/Requests####
Feel free to report any issues or feature requests you may have!
