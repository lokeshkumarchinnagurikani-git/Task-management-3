<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A&A Application</title>

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
width:450px;
background:#ffffff;
padding:25px;
border-radius:15px;
box-shadow:0 8px 20px rgba(0,0,0,0.2);
}

h2{
text-align:center;
color:#0066cc;
margin-bottom:10px;
}

.subtitle{
text-align:center;
font-size:15px;
color:#555;
margin-bottom:20px;
}

.input-area{
display:flex;
gap:10px;
margin-bottom:20px;
}

input{
flex:1;
padding:10px;
border:1px solid #ccc;
border-radius:5px;
font-size:15px;
}

button{
padding:10px 15px;
background:#007bff;
color:white;
border:none;
border-radius:5px;
cursor:pointer;
font-size:14px;
}

button:hover{
background:#0056b3;
}

ul{
list-style:none;
}

li{
display:flex;
justify-content:space-between;
align-items:center;
background:#eaf4ff;
padding:10px;
margin-bottom:10px;
border-radius:8px;
}

.completed{
text-decoration:line-through;
color:gray;
}

.actions button{
margin-left:5px;
padding:6px 10px;
}

.about{
margin-top:25px;
padding-top:15px;
border-top:2px solid #ddd;
text-align:center;
font-size:14px;
line-height:1.8;
color:#333;
}

.about h3{
color:#0066cc;
margin-bottom:10px;
}
</style>
</head>

<body>

<div class="container">

<h2>A&A Application</h2>

<p class="subtitle">
Developed by <b>Lokesh Kumar</b><br>
B.Tech (Electronics & Communication Engineering)<br>
Madanapalle Institute of Technology and Science
</p>

<div class="input-area">
<input type="text" id="taskInput" placeholder="Enter your task">
<button onclick="addTask()">Add</button>
</div>

<ul id="taskList"></ul>

<div class="about">
<h3>About Developer</h3>

<p><b>Name:</b> Lokesh Kumar</p>
<p><b>Course:</b> B.Tech - Electronics & Communication Engineering</p>
<p><b>College:</b> Madanapalle Institute of Technology and Science</p>
<p><b>Skills:</b> HTML, Python</p>
<p><b>Email:</b> lokeshkumarchinnagurikani@gmail.com</p>
<p><b>Platform Used:</b> This website was created and hosted using <b>GitHub Pages</b>.</p>

</div>

</div>

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

<div class="actions">
<button onclick="completeTask(this)">✔</button>
<button onclick="deleteTask(this)">🗑</button>
</div>
`;

document.getElementById("taskList").appendChild(li);

input.value="";
}

function completeTask(button){

button.parentElement.parentElement
.querySelector("span")
.classList.toggle("completed");

}

function deleteTask(button){

button.parentElement.parentElement.remove();

}

</script>

</body>
</html>
