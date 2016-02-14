## Demo of creating PDF from a HTML page with custom UTF font, using phantomjs 

## Notes
- Copy ila-sundaram-tamil-10.ttf to a web server
- Edit index.html to have correct url for ila-sundaram-tamil-10.ttf 

## RUN
~/programs/phantomjs-2.1.1-macosx/bin/phantomjs --output-encoding=utf8 html2pdf.js index.html index.pdf
