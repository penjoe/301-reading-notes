# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 12:**

### **Article:** [**EJS Partials**](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)

EJS Partials can be used to easily reuse parts of code. If you have something that will be used in several different sections or on different pages, making it a partial will allow you to write the code once and then just use `<%- include('/filepath') %>` to include that partial in your primary display page. This is especially useful for components like headers and nav bars thay you want to remain consistent throughout the your site. Or say you have a specific button that will be used. Making it a partial will require you to use write code only once, then just include it where you want it. PArtials are an extremely effective way to modularize your code and limit how much typing is required.

## **Additional resources:**
- [**EJS Partials Video from WalkThroughCode**](https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)