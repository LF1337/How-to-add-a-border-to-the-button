boarder to web3 git        boarder to web3 git
boarder to web3 git         boarder to web3 git
boarder to web3 git          boarder to web3 git
boarder to web3 git      boarder to web3 git
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Warecolaroal</title>
    <link rel="stylesheet" href="./index.css">
</head>
<body>
    <button id="btn">hide</button>
    <h1 id="title">hi 1</h1>
    <div id="result"></div>
    <script src="./index.js"></script>
</body>
</html>

------


    body {
    font-family: Arial, sans-serif;
    background: url('sit') no-repeat center center fixed;
    background-size: cover;
    text-align: center;
    padding: 20px;
    color: white; 
}

h1, h2 {
    color: white; 
}

button {
    background-color: rgba(0, 123, 255, 0.8); 
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    margin: 20px 0;
    border-radius: 5px;
}

button:hover {
    background-color: rgba(0, 86, 179, 0.8);
}

.displayNone {
    display: none;
}

#result {
    margin-top: 20px;
}

----


let counter = 1;
const title = document.getElementById('title');
const btn = document.getElementById('btn');
const result = document.getElementById('result');
const maxHeadings = 5; 

function createHeading(text) {
    let heading = document.createElement('h2');
    heading.setAttribute('id', `heading${counter}`);
    heading.textContent = text;
    heading.style.color = 'white'; 
    return heading;
}

btn.addEventListener('click', () => {
    if (title.className === 'displayNone') {
        btn.innerHTML = 'hide';
        title.classList.remove('displayNone');
    } else {
        title.classList.add('displayNone');
        btn.innerHTML = 'show';
    }

    if (counter <= maxHeadings) {
        let heading = createHeading(`Heading ${counter}`);
        counter++;
        result.appendChild(heading);
    } else {
        alert('Maximum number of headings reached.');
    }
});
