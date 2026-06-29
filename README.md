# lokesh kumar 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Task Management App</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:#f4f7fc;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
}

.container{
width:420px;
background:white;
padding:20px;
border-radius:10px;
box-shadow:0 5px 10px rgba(0,0,0,.2);
}

h2{
text-align:center;
margin-bottom:20px;
color:#007bff;
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
}

button{
padding:10px 15px;
background:#007bff;
color:white;
border:none;
border-radius:5px;
cursor:pointer;
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
padding:10px;
margin-bottom:10px;
background:#eaf2ff;
border-radius:5px;
}

.completed{
text-decoration:line-through;
color:gray;
}

.actions button{
margin-left:5px;
padding:5px 10px;
}
</style>
</head>

<body>

<div class="container">

<h2>Task Management App</h2>

<div class="input-area">
<input type="text" id="taskInput" placeholder="Enter Task">
<button onclick="addTask()">Add</button>
</div>

<ul id="taskList"></ul>

</div>

<script>
function addTask(){

let input=document.getElementById("taskInput");

let task=input.value.trim();

if(task===""){
alert("Enter a task");
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

function completeTask(btn){
btn.parentElement.parentElement.querySelector("span").classList.toggle("completed");
}

function deleteTask(btn){
btn.parentElement.parentElement.remove();
}
</script>

</body>
</html>
