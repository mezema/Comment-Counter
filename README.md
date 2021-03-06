# This script helps automate checks on when the code is merged into the build pipeline.

#Assumptions: 
- """triple quotes""" is not a multiline comment in python instead its a docstring.
- Program file is written in Python, Java, Javascript, C or SQL
- Input come in form of a filepath
- Block comments in python always start with # without white spaces
- File has extension and does not start with a ‘.’

The define automate_checks() function takes in the filepath to the program file as input and returns the following outputs:
- Total # of lines
- Total # of comment lines
- Total # of single line comments
- Total # of comment lines within block comments
- Total # of block line comments
- Total # of TODO’s

It makes use of two helper functions quote_check() and quote_check_multiple(). quote_check() takes in the line and target character as input and returns True if target character is not inbetween quotation marks. quote_check_multiple() takes in a line and target string as input and returns True if target string is not inbetween quotation marks.

We begin by opening the file in the default read mode. We the get list of all lines in file and count the number of lines in the program file by getting the length of the list of all lines.
This approach works well for reasonably sized files so I am assuming the file is of a reasonable size.

We check if its a Python, Javascript, C, Java or SQL file.

We iterate through the list of lines and remove all white space from the beginning (left trimming) and perform the necessary checks.

We then close the file to manage resources
