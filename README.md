<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sannay's Compiler</title>
    <style>
body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    background: yellowgreen;
}
header {
    height: 200px;
    background: #7b922e;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: -15px;
}
section{
    max-width: 800px;
    margin: 2em auto;
    padding: 1em;
}
textarea{
    width: 100%;
    height: 400px;
    font-size: 30px;
}
button{
    display: block;
    color: yellow;
    margin: 1em auto;
    background: blue;
    padding: 0.5em 1em;
    border-radius: 25px;
    font-size: 1em;
    cursor: pointer;
    border: 2px solid black;
    box-shadow:5px 4px 5px #000 ;
    transition: 1s; 
}
button:hover {
    color: blue;
    background: yellow;
   } 

iframe{

width: 100%;
height: 200px;
}

    </style>
</head>
<body>
    <header>
        <img src="c:\Users\hassaan haider\Downloads\72173f6a-b1da-45f6-8cf4-6bf0247d335d.jpg" 
        alt="logos" width="20%" height="100%"style="margin-left:-150px;" >
        <a href="https://www.facebook.com/profile.php?id=61550353705124&mibextid=ZbWKwL"><svg style="color: blue ;margin:30px;" xmlns="http://www.w3.org/2000/svg" width="80" height="80" fill="currentColor" class="bi bi-facebook" viewBox="0 0 16 16">
            <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z" fill="blue"></path> </svg>
           </a> 
        <a href="https://youtube.com/@HassaanHaider-kf9st?si=HnAsWn9Slcz-lgYN"><svg style="color: red ;margin:30px;" xmlns="http://www.w3.org/2000/svg" width="80" height="80" fill="currentColor" class="bi bi-youtube" viewBox="0 0 16 16"> 
            <path d="M8.051 1.999h.089c.822.003 4.987.033 6.11.335a2.01 2.01 0 0 1 1.415 1.42c.101.38.172.883.22 1.402l.01.104.022.26.008.104c.065.914.073 1.77.074 1.957v.075c-.001.194-.01 1.108-.082 2.06l-.008.105-.009.104c-.05.572-.124 1.14-.235 1.558a2.007 2.007 0 0 1-1.415 1.42c-1.16.312-5.569.334-6.18.335h-.142c-.309 0-1.587-.006-2.927-.052l-.17-.006-.087-.004-.171-.007-.171-.007c-1.11-.049-2.167-.128-2.654-.26a2.007 2.007 0 0 1-1.415-1.419c-.111-.417-.185-.986-.235-1.558L.09 9.82l-.008-.104A31.4 31.4 0 0 1 0 7.68v-.123c.002-.215.01-.958.064-1.778l.007-.103.003-.052.008-.104.022-.26.01-.104c.048-.519.119-1.023.22-1.402a2.007 2.007 0 0 1 1.415-1.42c.487-.13 1.544-.21 2.654-.26l.17-.007.172-.006.086-.003.171-.007A99.788 99.788 0 0 1 7.858 2h.193zM6.4 5.209v4.818l4.157-2.408L6.4 5.209z" fill="red"></path> </svg>
            </a>
            <h1 style="display: inline; margin-right: -20px; margin-right: 20px;">Online Compiler</h1>

        <a href="https://hassaanhaidersspace.quora.com/?ch=10&oid=4326410&share=396067ef&srid=33zGOd&target_type=tribe"><svg style="color: red ;margin:30px;" xmlns="http://www.w3.org/2000/svg" width="80" height="80" fill="currentColor" class="bi bi-quora" viewBox="0 0 16 16"> 
            <path d="M8.73 12.476c-.554-1.091-1.204-2.193-2.473-2.193-.242 0-.484.04-.707.142l-.43-.863c.525-.45 1.373-.808 2.464-.808 1.697 0 2.568.818 3.26 1.86.41-.89.605-2.093.605-3.584 0-3.724-1.165-5.636-3.885-5.636-2.68 0-3.839 1.912-3.839 5.636 0 3.704 1.159 5.596 3.84 5.596.425 0 .811-.046 1.166-.15Zm.665 1.3a7.127 7.127 0 0 1-1.83.244C3.994 14.02.5 11.172.5 7.03.5 2.849 3.995 0 7.564 0c3.63 0 7.09 2.828 7.09 7.03 0 2.337-1.09 4.236-2.675 5.464.512.767 1.04 1.277 1.773 1.277.802 0 1.125-.62 1.179-1.105h1.043c.061.647-.262 3.334-3.178 3.334-1.767 0-2.7-1.024-3.4-2.224Z" fill="red"></path> </svg>
            </a>
       <a href="https://www.tiktok.com/@hassaan_haider88?_t=8htMroS8juz&_r=1"><svg style="margin:30px;" xmlns="http://www.w3.org/2000/svg" width="80" height="80" fill="black" class="bi bi-tiktok" viewBox="0 0 16 16"> 
        <path d="M9 0h1.98c.144.715.54 1.617 1.235 2.512C12.895 3.389 13.797 4 15 4v2c-1.753 0-3.07-.814-4-1.829V11a5 5 0 1 1-5-5v2a3 3 0 1 0 3 3V0Z"/> </svg>
        </a> 

        
    </header>
    <section id="editor-section">
        <h2 style="font-size: 40px;">Code Editor</h2>
        <textarea id="code" placeholder="write html css and javascript code here...." 
        style=" box-shadow:5px 4px 5px #000 ;border-radius: 30px;padding: 15px; "></textarea>
    </section>
    <button id="compile-run-btn" onclick="compileAndRun()">Compile & run</button>
    <section id="output-section" >
        <h2>output</h2>
        <iframe style="background: white; border-radius: 30px; box-shadow:5px 4px 5px #000 ; 
        " id="output"></iframe>
    </section>
    <div>
        <h1> Learning the Basics of HTML, CSS, and JavaScript A Beginner's Guide :</h1>
        

<p style="text-indent: 25px;">In the world of web development, mastering the trio of HTML, CSS, and JavaScript lays the foundation for creating 
    stunning and interactive websites. Whether you're a complete beginner or looking to refresh
     your skills, here's a step-by-step guide on how to learn HTML, CSS, and JavaScript in the basics.</p>

<h1 style="color: #a09393;"> HTML (HyperText Markup Language) </h1>

<h2> 1. Understand the Basics:</h2>
   <li> HTML is the backbone of web development, providing the structure for web pages.</li>
   <li> Learn about HTML tags, elements, attributes, and their hierarchical structure.</li>
   <li> Explore commonly used tags like "&lt;html &gt;", "&lt;head &gt;", "&lt;body&gt;", "&lt;p&gt;", "&lt;div&gt;", and more.</li>

<h2> 2. Build Your First Web Page: </h2>
   <li> Create a simple HTML document using a text editor like Notepad or Visual Studio Code.</li>
   <li>Include headings, paragraphs, lists, and links to practice the fundamentals.</li> 
   <li> Understand the DOCTYPE declaration and the importance of well-formed HTML.</li>

<h2> 3. Study HTML Forms: </h2>
   <li> Explore form elements such as "&lt;input&gt;", "&lt;textarea&gt;", "&lt;select&gt;", and "&lt;button&gt;".</li>
   <li>Learn how to collect user input and submit forms. </li>

<h1 style="color: #a09393;"> CSS (Cascading Style Sheets)</h1>

<h2> 1. Grasp the Basics of Styling: </h2>
   <li> CSS is used for styling HTML elements and enhancing the visual appeal of a website.</li>
   <li> Understand selectors, properties, and values.</li>
   <li> Experiment with basic styling properties like color, font-size, margin, and padding.</li>

<h2> 2. Practice Selectors: </h2>
   <li> Learn about different types of selectors, including element selectors, class selectors, and ID selectors.</li>
   <li> Understand the concept of specificity in CSS.</li>

<h2> 3. Create Responsive Designs: </h2>
   <li>Study the principles of responsive design using media queries.</li>
   <li>Make your web pages adapt to different screen sizes by applying responsive styling.</li> 

<h1 style="color: #a09393;"> JavaScript</h1>

<h2> 1. Grasp the Basics of JavaScript: </h2>
   <li>JavaScript adds interactivity and dynamic behavior to web pages.</li> 
   <li> Start with basic concepts such as variables, data types, and operators.</li>
   <li> Learn how to use `console.log()` for debugging.</li>

<h2> 2. Understand Control Flow:</h2>
   <li> Study conditional statements (`if`, `else`, `switch`) and loops (`for`, `while`) to control program flow.</li>
   <li> Learn about truthy and falsy values.</li>

<h2> 3. Manipulate the DOM (Document Object Model):</h2>
   <li>Understand how JavaScript interacts with the DOM. </li>
   <li>Learn to select and manipulate HTML elements using JavaScript.</li> 
   <li>Practice event handling to respond to user actions.</li>

<h1 style="color: #a09393;">Practice and Build Projects:</h1> 

<h2>1. Build Simple Projects:</h2>
   <li> Apply what you've learned by building small projects.</li>
   <li> Create a personal portfolio page, a to-do list app, or a simple calculator.</li>

<h2> 2. Explore Online Resources: </h2>
   <li> Utilize online platforms like MDN Web Docs, W3Schools, and freeCodeCamp for in-depth tutorials and exercises.</li>
   <li>Follow coding challenges on platforms like HackerRank and CodeSignal.</li> 

<h2>3. Join Coding Communities:</h2>
   <li> Engage with coding communities on platforms like Stack,Overflow or Reddit.</li>
   <li> Attend local meetups or online web development forums.</li>

<h1 style="color: #a09393;"> Conclusion: </h1>
Learning HTML, CSS, and JavaScript is an exciting journey that opens the doors to web development. Approach it step by step, practice consistently, and don't hesitate to seek help from the vast online community. With dedication and hands-on experience, you'll soon be creating your own web projects and 
contributing to the dynamic world of web development. Happy coding!
    </div>
</body> 
<script>
function compileAndRun(){
    const code=
    document.getElementById("code").value;
    const outputFrame=
    document.getElementById("output");
const outputDoc= 
outputFrame.contentDocument || outputFrame.contentWindow.document; 
outputDoc.open();
outputDoc.write(code);
outputDoc.close();

}

</script>
</html>
