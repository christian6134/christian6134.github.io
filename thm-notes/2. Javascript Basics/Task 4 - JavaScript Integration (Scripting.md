
## JavaScript Integration with HTML – Notes

### 🌐 Basic Overview

- JavaScript (JS) is used with HTML and CSS to make web pages dynamic and interactive.
    
- It does **not** render content like HTML but enhances interactivity.
    
- If you're unfamiliar with HTML, it's recommended to review it first.
    

---

## 🔗 Two Main Ways to Integrate JS into HTML

### 1. **Internal JavaScript**

- JS code is **embedded directly** into the HTML file using `<script>` tags.
    
- Preferred for **beginners** since it allows easy experimentation.
    

**Placement of `<script>` tags:**

- Inside `<head>`: For scripts that need to load before the page content.
    
- Inside `<body>`: For scripts interacting with page elements as they load.
    

**Example:**

html

CopyEdit

`<!DOCTYPE html> <html lang="en"> <head>     <title>Internal JS</title> </head> <body>     <h1>Addition of Two Numbers</h1>     <p id="result"></p>      <script>         let x = 5;         let y = 10;         let result = x + y;         document.getElementById("result").innerHTML = "The result is: " + result;     </script> </body> </html>`

- The result is dynamically inserted into the `<p>` element with id="result".
    

---

### 2. **External JavaScript**

- JS code is **stored in a separate file** with a `.js` extension.
    
- Promotes **cleaner**, more **organized** code.
    
- Reusable across multiple HTML pages.
    

**Steps:**

1. Create `script.js`:
    

let x = 5; let y = 10; let result = x + y; document.getElementById("result").innerHTML = "The result is: " + result;`

2. Create `external.html`:
    

`<!DOCTYPE html> <html lang="en"> <head>     <meta charset="UTF-8">     <title>External JS</title> </head> <body>     <h1>Addition of Two Numbers</h1>     <p id="result"></p>      <script src="script.js"></script> </body> </html>`

- Output will be the same as the internal example.
    
- The JS code is pulled in via the `src` attribute of the `<script>` tag.
    

---

## 🕵️ How to Verify JS Type (Internal vs. External)

**To view source code in Chrome:**

- Right-click on the page → Select **"View Page Source"**.
    

**Check for:**

- `<script>` **without** `src` → Internal JS
    
- `<script src="...">` → External JS
    

**Try it:**

- Open `external_test.html` and inspect how JS is loaded.
    
- Visit [TryHackMe.com](https://tryhackme.com), right-click, and choose “View Page Source” to explore how JS is used.
    

---

## ✅ Quick Review Questions

|Question|Answer|
|---|---|
|Which JS integration places code directly in HTML?|**Internal**|
|Which method is better for reusing JS across multiple pages?|**External**|
|What is the name of the external JS file used by `external_test.html`?|**thm_external.js**|
|What attribute links an external JS file in the `<script>` tag?|**`src`**|