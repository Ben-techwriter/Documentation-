# How to Build a Simple Website with HTML and CSS


## Project Structure 

```mermaid
graph TD;
IndexHTML-->StyleCSS;
StyleCSS--->SimpleWebpage
````


### Step1: Create the HTML file 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Simple Web Page</title>
    styles.css
</head>

<body>

    <header class="hero">
        <h1>Welcome to My Web Page</h1>
        <p>This is a simple example page built using HTML & CSS.</p>
    </header>

    <section class="content">
        <h2>About This Tutorial</h2>
        <p>
            In this tutorial, you learned how to create a clean and modern webpage.
            You can continue by adding images, links, buttons, and more.
        </p>
    </section>

</body>
</html>


````



### Step 2: Add Styling with CSS

```
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #fafafa;
}

.hero {
    background: #4a90e2;
    color: white;
    text-align: center;
    padding: 80px 20px;
}

.content {
    max-width: 800px;
    margin: 40px auto;
    background: white;
    padding: 20px 30px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}


```



### Step 3: The final Outcome 



### Step 4: Explain Key Concepts 

1. The HTML Structure

<header> is used for the top banner.
<section> organizes content into readable parts.
<link rel="stylesheet"> connects your CSS file.

2. The CSS Styling

background: #4a90e2 adds color to the hero section.
box-shadow creates a subtle card effect.
max-width keeps text readable.

3. Responsive Features

meta viewport makes the site mobile-friendly.
Padding and font sizes scale well on all screens.

### Step 5: Run the Project 
Simply open index.html in your browser:


You’ve successfully created a clean webpage using HTML & CSS — and documented it professionally.


