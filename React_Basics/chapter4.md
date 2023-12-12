# Chapter 4 - Getting Started with React

Things to know:
- **react** - the core React library
- **react-dom** - provides DOM-specific methods that enable you to use React with the DOM

Before you start using react, you need to download the packages here: [UNPKG](https://unpkg.com/)

So now it should look like this in the lines 4-5: 

```html
<html>
  <body>
    <div id="app"></div>
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script type="text/javascript">
      const app = document.getElementById('app');
      const header = document.createElement('h1');
      const text = 'Develop. Preview. Ship.';
      const headerContent = document.createTextNode(text);
      header.appendChild(headerContent);
      app.appendChild(header);
    </script>
  </body>
</html>
```
