# Archive-Documentation

## How To

# PDF Creation from Images

SW 22 Sept 2016 - free and open source, Linux based workflow

## Scan and image batch cleanup

http://scantailor.org/

## Use imagemagic to bundle pics into PDF

This includes PDF optimisation

http://askubuntu.com/questions/493584/convert-images-to-pdf/557975

convert "*.{png,jpeg}" outfile.pdf
Optionally you can combine more files into one pdf file with including them inside {} and separate them with a single comma.

convert "*.{ext1,ext2,ext3,...}" outfile.pdf

convert "*.{tif}" M000-master.pdf

## Add bookmarks and basic metadata

### Bookmarks

Add Bookmarks in a PDF file with Ghostscript

http://ask.xmodulo.com/add-bookmarks-pdf-document-linux.html

gs -sDEVICE=pdfwrite -q -dBATCH -dNOPAUSE -sOutputFile=output.pdf -dPDFSETTINGS=/prepress index.info -f input.pdf

add an index.info file

[/Page 1 /Title (Front Page) /OUT pdfmark
[/Page 24 /Title (Back Page) /OUT pdfmark

### Metadata

Use Ghostview

See https://askubuntu.com/a/723078

create a file 'pdfmarks' with your metadata and then run the command line script below to merge the metadata with your PDF.

run

gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/prepress -dNOPAUSE -dQUIET -dBATCH -sOutputFile=M002-ISSN-1356-7748-03.pdf M002-resource.pdf pdfmarks

## OCR

Skipped for the moment as free and open source systems don't work well. Help appreciated :-)

Benchmark (03.11.16)

https://github.com/tesseract-ocr/tesseract

GOCR and Cuneiform are also worth to try: launchpad.net/cuneiform-linux jocr.sourceforge.net

poppler to parse PDFs used for PDF2FXL EPUB3 conversion


