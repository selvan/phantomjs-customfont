## Demo of creating PDF from a HTML page with custom UTF font, using phantomjs 

## Notes
- Copy ila-sundaram-tamil-10.ttf to a web server
- Edit index.html to have correct url for ila-sundaram-tamil-10.ttf 

## RUN
~/programs/phantomjs-2.1.1-macosx/bin/phantomjs --output-encoding=utf8 html2pdf.js index.html index.pdf

## Hacker Notes
- Phantomjs is written in C++ & exposes C++ objects (such as WebPage, src/webpage.cpp) via Javascript API
- Phantomjs depends on Qt (Qt wraps Webkit engine)
- PDF printing is done by renderPdf method of https://github.com/ariya/phantomjs/blob/master/src/webpage.cpp 
- renderPdf method uses various Qt related objects such as QPrinter, QWebFrame etc
- For PDF printing, it is possible to use python binding such as PyQt, to achieve same result
