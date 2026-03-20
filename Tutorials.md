# How to Build a Simple Website with HTML and CSS


## Project Structure 

```mermaid
graph TD;
IndexHTML-->StyleCSS;
StyleCSS--->SimpleWebpage
````

## Steps
1. Create an html file with the code given below and save it as index.html.
2. Create a css file with the code given below and save it as styles.css.
3. Ensure to reference the css file in the html file.
4. Click the html file and it opens as website with the text and styling specified.
5. You have created a static website. 

### Step1: Create the HTML file 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Simple Web Page</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>

    <header class="hero">
        <h1>Welcome to My Web Page</h1>
        <p>I have created this page to showcase my expertise in using HTML and CSS.</p>
    </header>

    <section class="content">
        <h2>About ME</h2>
        <p>
             This page provides a brief view of myself, my skill sets and overall exprtise. 
	<buttton> Click to know more</button>
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
    background: #c6cee2;
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

<img width="1828" height="706" alt="image" src="https://github.com/user-attachments/assets/68d9930e-b610-460b-b542-d582b0957975" />



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


