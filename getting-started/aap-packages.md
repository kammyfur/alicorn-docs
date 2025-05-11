# AAP packages

Alicorn uses AAP (Alicorn Application Package) folders; these folders are considered as files throughout the system. Within this AAP folder, you can include all your app's source code and resources. This effectively makes managing apps for the end user easier, as they behave like they are individual files.

The typical structure for an AAP package is as follows:

* com.example.aap
  * AlicornApp.svg
  * AlicornApp.json
  * index.html
  * main.js
  * css
    * style1.css
    * style2.css
  * js
    * script1.js
    * script2.js
    * lib.js
  * assets
    * icon.png

The only hard requirements are:

* the icon must be either AlicornApp.svg or AlicornApp.png
* the metadata file must be AlicornApp.yml
* the main page file must be index.html
