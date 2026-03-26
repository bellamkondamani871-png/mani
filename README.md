<!DOCTYPE html>
<html>
<head>
  <title>Exam Hall Ticket</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #f2f2f2;
    }
    .box {
      background: white;
      padding: 20px;
      width: 300px;
      margin: auto;
      border-radius: 10px;
    }
    input, button {
      margin: 10px;
      padding: 10px;
      width: 90%;
    }
  </style>
</head>
<body>

<h2>Exam Hall Ticket Booking</h2>

<div class="box">
  <input type="text" id="name" placeholder="Enter Name"><br>
  <input type="text" id="roll" placeholder="Enter Roll Number"><br>
  <input type="date" id="dob"><br>
  <button onclick="generateTicket()">Get Hall Ticket</button>
</div>

<div id="ticket"></div>

<script>
function generateTicket() {
  let name = document.getElementById("name").value;
  let roll = document.getElementById("roll").value;
  let dob = document.getElementById("dob").value;

  if(name=="" || roll=="" || dob==""){
    alert("Fill all details!");
    return;
  }

  document.getElementById("ticket").innerHTML = `
    <h3>Hall Ticket</h3>
    <p>Name: ${name}</p>
    <p>Roll No: ${roll}</p>
    <p>DOB: ${dob}</p>
    <p>Exam Center: ABC College</p>
    <button onclick="window.print()">Download / Print</button>
  `;
}
</script>

</body>
</html>
