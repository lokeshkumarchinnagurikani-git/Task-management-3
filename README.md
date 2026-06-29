<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>T&M Application</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:skyblue;
display:flex;
justify-content:center;
align-items:center;
min-height:100vh;
padding:20px;
}

.container{
max-width:700px;
width:100%;
background:#fff;
padding:30px;
border-radius:15px;
box-shadow:0 8px 20px rgba(0,0,0,0.2);
}

h1{
text-align:center;
color:#0056b3;
margin-bottom:10px;
}

h2{
color:#007bff;
margin-top:20px;
margin-bottom:10px;
}

p{
font-size:16px;
line-height:1.8;
color:#333;
}

.info{
background:#f2f8ff;
padding:15px;
border-radius:10px;
margin-top:15px;
}

.footer{
margin-top:25px;
text-align:center;
font-size:14px;
color:#555;
}
</style>
</head>

<body>

<div class="container">

<h1>T&M Application</h1>

<p>
Welcome to my personal website. This webpage introduces me and provides information about the platform used to create and host this website.
</p>

<h2>About Me
a authentication</h2>

<div class="info">
<p><b>Name:</b> Lokesh Kumar</p>
<p><b>Course:</b> B.Tech - Electronics and Communication Engineering (ECE)</p>
<p><b>College:</b> Madanapalle Institute of Technology and Science</p>
<p><b>Skills:</b> HTML, Python</p>
<p><b>Email:</b> lokeshkumarchinnagurikani@gmail.com</p>
<p><b>Career Goal:</b> To improve my web development and programming skills while building useful applications.</p>
</div>

<h2>About GitHub</h2>

<div class="info">
<p>
The Authorization 
GitHub is a cloud-based platform used for storing, managing, and sharing source code through Git version control.
</p>

<p>
GitHub which allows developers to publish websites directly from a GitHub repository for free of cost also.
</p>

<p>
GitHub helps developers collaborate on projects, track code changes, and maintain different versions of applications efficiently.
</p>
</div>

<div class="footer">
<p><b>Developed by Lokesh Kumar</b></p>
<p>Powered by GitHub Pages</p>
    <h2>Task Manager</h2>

<div class="input-area">
    <input type="text" id="taskInput" placeholder="Enter a new task">
    <button onclick="addTask()">Add Task</button>
</div>

<ul id="taskList"></ul>
.input-area{
display:flex;
gap:10px;
margin-top:15px;
margin-bottom:20px;
}

.input-area input{
flex:1;
padding:10px;
border:1px solid #ccc;
border-radius:5px;
}

.input-area button{
padding:10px 15px;
background:#007bff;
color:white;
border:none;
border-radius:5px;
cursor:pointer;
}

.input-area button:hover{
background:#0056b3;
}

#taskList{
list-style:none;
padding:0;
}

#taskList li{
display:flex;
justify-content:space-between;
align-items:center;
background:#eaf4ff;
padding:10px;
margin-top:10px;
border-radius:5px;
}

.completed{
text-decoration:line-through;
color:gray;
}
<script>
function addTask(){

let input=document.getElementById("taskInput");
let task=input.value.trim();

if(task===""){
alert("Please enter a task.");
return;
}

let li=document.createElement("li");

li.innerHTML=`
<span>${task}</span>
<div>
<button onclick="this.parentElement.parentElement.querySelector('span').classList.toggle('completed')">✔</button>
<button onclick="this.parentElement.parentElement.remove()">🗑</button>
</div>
`;

document.getElementById("taskList").appendChild(li);

input.value="";
}
</script>

</div>

</div>

</body>
</html>  
