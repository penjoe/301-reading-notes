# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 11:**

### **Video:** [**EJS Tutorial from WalkThroughCode**](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)

- EJS is a simple templating language that lets you generate HTML markup with plain JavaScript
-  similar to how mustache.js is a template, creates new `views` in the html
-  works form a separate .ejs file, similar to how a .html file would be used
-  EJS syntax is wrapped in `<% %>`
-  variables can be passed in to EJS 
    -  variable can be any JS data type
    -  `=` is used to valuate variable
- JS can be written directly into the .ejs file as long as it is inside of the EJS syntax `<% %>`
- JS conditional `if/else` statements can be injected into the EJS syntax
- layouts are not native to EJS but can be used with a separate npm package `express-ejs-layouts`
    - creates a placeholder for all the views withing the layout. acts as the 'wrapper' for the EJS content
    -  require `.get` route to layout.ejs file
- partials are native to EJS
    - makes a reusable piece of code
    - useful for things like footers or navs
    


## **Additional resources:**
- [**Google Books API Docs**](https://developers.google.com/books/docs/v1/using#WorkingVolumes)
- [**EJS Docs**](https://ejs.co/)
- [**EJS Tutorial**](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)
  - [Source code for EJS tutorial](https://github.com/scotch-io/node-ejs) - review along with tutorial