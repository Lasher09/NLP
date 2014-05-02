**Program:** PyPdf 

*Purpose and Description:* This is a simple script for manipulating PDF files. There are several other functions include with PyPdf. This should get you started. Before beginning, make sure PyPdf is installed on your system.

**Program Capabilities:** Print the title of a PDF document, the number of pages, and the contents of the file into a new PDF file.

**Code:**
```
# Code copied from http://pybrary.net/pyPdf/

from pyPdf import PdfFileWriter, PdfFileReader

output = PdfFileWriter()
input1 = PdfFileReader(file("document1.pdf", "rb"))

# print the title of document1.pdf
print "title = %s" % (input1.getDocumentInfo().title)

# add page 1 from input1 to output document, unchanged
output.addPage(input1.getPage(0))

# print how many pages input1 has:
print "CV.pdf has %s pages." % input1.getNumPages()

# finally, write "output" to document-output.pdf
outputStream = file("document-output.pdf", "wb")
output.write(outputStream)
outputStream.close()

```

**Output:** Output will vary depending on the content of the PDF file.