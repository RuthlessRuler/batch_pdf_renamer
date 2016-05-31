# PDF batch renamer
This program tries to batch rename PDF files if an ISBN number is found in its first 10 pages.

This package should not be installed. Instead it should be used with command line.
Use
`python3 main.py --help`
for complete arguments list.

## Usage
`python3 main.py --input /folder/to/scan/for/pdfs`

This will scan the input folder for pdfs and rename them based on the ISBN number found in each of these files.

Optionally the user can use the '--use-metadata' argument to get the author and title fields embedded in the pdf.

A nice feature is the file 'restorelog.txt': if you use a Unix system and you don't like the results you can revert them pasting the lines generated by the program in this file.

You can also try a dry-run before actually using it (argument --dry-run).
## Dependencies
1. PyPDF2
2. isbnlib

*PyPDF2* is used to get the text from the first 10 pages of your pdf.

*isbnlib* is used to query the ISBN number found (if any).

## TODO
- remove the `import *` statement
