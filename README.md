# Onee.chFE
The Onee.ch frontend. 

Live site: <a href="https://onee.ch" target="blank">onee.ch</a>

<h3>Setting a favicon</h3>
enter this. Make sure you remove the curly brackets. <br>
mongofiles -h localhost -d {DBname} -l {/path/to/favicon.ico} put /favicon.ico

<h3>Making the archive link work</h3>
Add a new line before line 120 in /home/sen/LynxChan/src/be/data/defaultPages.json and paste this:
"linkArchive": "href",

Change lines 459 and 460 in LynxChan/src/be/engine/domManipulator/static.js to:
    .replace('__linkLogs_href__', '/logs.js?boardUri=' + boardData.boardUri)
	  .replace('__linkArchive_href__', '/archives.js?boardUri=' + boardData.boardUri);
