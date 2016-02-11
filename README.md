# PyBuilder
####What Is It?####
pyBuilder is a Static HTML Generation Engine, allowing you to dynamically include multiple files (templates) within an HTML document. Because PyBuilder statcially generates the HTML documents after running, any inclusions can be used (.html, .js, .php, etc.).

####How It Works####
PyBuilder parses a file at build time to look for file dependencies, noted in the file by using
```
  <include file="path/to/file[.html][.js][.php]"/>
```
At this time, PyBuilder reads and inserts the dependent file into the parent file, building an entirely new file (with the same name) inside a newly created build/ directory.

####Basic Usage####
- Add pb.py to your project directory
- Run: ```python3 pb.py```
- This will build all files in PyBuilder's directory, copy all assets, and add them to a build/ directory
- Note: We recommend placing pyBuilder at the beginning of your directory (with your main HTML files), as the ```<include>``` tags currently read file location relative to the builder's location within your directory structure.

####Arguments####
- Build Single File: 
```
-f FILENAME or --file=FILENAME
```
- Modify destination directory:
```
-d DESTINATION or --destination=DESTINATION
```

####Bugs/Requests####
Feel free to report any issues or feature requests you may have!

####Updates####
- 02/10/16 - Modifies command line syntax structure and adds error checking
- 02/04/16 - PyBuilder now copies all assets into the build/ directory.
- 01/13/16 - Moved to command-line argument model rather than utilizing python's input() function.
