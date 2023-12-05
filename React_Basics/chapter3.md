# Chapter 3 - Updating UI with Javascript

Lets start using the DOM, make an index.html file and enter the following: 


```Html
<html>
  <body>
    <div id="app"></div>
  </body>
</html>
```

---
You have given the div a unique ID, so now add the script tag
```Html
<html>
  <body>
    <div id="app"></div>
    <script type="text/javascript"></script>
  </body>
</html>
```


---
Now, inside the script tag, you can use a DOM method, getElementById(), to select the <div> element by its id:

```Html
<html>
  <body>
    <div id="app"></div>
    <script type="text/javascript">
      const app = document.getElementById('app');
    </script>
  </body>
</html>
```


---
Using DOM, you can even make a whole new h1, changing the content of your file
```html
<html>
  <body>
    <div id="app"></div>
    <script type="text/javascript">
      // Select the div element with 'app' id
      const app = document.getElementById('app');
 
      // Create a new H1 element
      const header = document.createElement('h1');
 
      // Create a new text node for the H1 element
      const text = 'Develop. Preview. Ship. 🚀';
      const headerContent = document.createTextNode(text);
 
      // Append the text to the H1 element
      header.appendChild(headerContent);
 
      // Place the H1 element inside the div
      app.appendChild(header);
    </script>
  </body>
</html>
```

---
Now, you will notice one thing of these two images, the DOM of the page is different from the HTML file you made.
![DOM](html-compare-dom.avif)
This is because the HTML represents the initial page, and the DOM represents the updated page content after the Javascrpt code.

Updating the DOM with plain JavaScript is very powerful but verbose. You've written all this code to add an h1 element with some text:

```html
<script type="text/javascript">
  const app = document.getElementById('app');
  const header = document.createElement('h1');
  const text = 'Develop. Preview. Ship. 🚀';
  const headerContent = document.createTextNode(text);
  header.appendChild(headerContent);
  app.appendChild(header);
</script>
```

One thing to mention, as more and more people contribute to projects, the more difficult it is in order to manage it. Due to this, most coding is just telling the computer what to do. 

---
## What if we could describe what it is that you want to show and let the computer figure out how to update the DOM

- Imperative vs. declarative programming

The code above is a demonstration of **imperative programming**. Merely writing the instructions. But when it comes to building user interfaces, a **declarative** approach is often preferred because it can speed up the development process. Rather than writing DOM methods, it would be helpful if developers were able to declare what they want to show.

In other words, imperative programming is like giving a chef step-by-step instructions on how to make a pizza. Declarative programming is like ordering a pizza without being concerned about the steps it takes to make the pizza. Leaving it up to the computer. 