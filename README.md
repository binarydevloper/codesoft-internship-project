# codesoft-internship-project
<!DOCTYPE html>
<html lang="en">
<head>
   <style>
      *{
         padding: 0;
         margin: 0;
         font-family: 'poppins', sans-serif;
      }
      body{
         background-color: #f199d8;
         display: grid;
         height: 100vh;
         place-items: center;
      }
      .main{
         width: 400px;
         height: 450px;
         background-color: rgb(248, 196, 24);
         position: absolute;
         border: 5px solid rgb(9, 9, 9);
         border-radius: 6px; 
      }
      .main input[type='text'] {
         width: 88%;
         position: relative;
         height: 80px;
         top: 5px;
         text-align: right;
         padding: 3px 6px;
         outline: none;
         font-size: 40px;
         border: 5px solid black;
         display: flex;
         margin: auto;
         border-radius: 6px;
         color: rgb(47, 44, 81);
      }
      .btn input[type='button']{
         width:90px;
         padding: 2px;
         margin: 2px 0px;
         position: relative;
         left: 13px;
         top: 20px;
         height: 60px;
         cursor: pointer;
         font-size: 18px;
         transition: 0.5s;
         background-color: #010f10;
         border-radius: 6px;
         color: white;
      }
      .btn input[type='button']:hover{
         background-color: black;
         color: white;
      }
   </style>
   <script>
      function Solve(val) {
         var v = document.getElementById('res');
         v.value += val;
      }
      function Result() {
         var num1 = document.getElementById('res').value;
         var num2 = eval(num1);
         document.getElementById('res').value = num2;
      }
      function Clear() {
         var inp = document.getElementById('res');
         inp.value = '';
      }
      function Back() {
         var ev = document.getElementById('res');
         ev.value = ev.value.slice(0,-1);
      }
   </script>
   <title>Calulator</title>
</head>
<body>
   <div class="main">
      <input type="text" id = 'res'>
      <div class="btn">
         <input type="button" value = 'C' onclick = "Clear()">
         <input type="button" value = '%' onclick = "Solve('%')">
         <input type="button" value = '←' onclick ="Back('←')">
         <input type="button" value = '/' onclick = "Solve('/')">
         <br>
         <input type="button" value = '7' onclick = "Solve('7')">
         <input type="button" value = '8' onclick = "Solve('8')">
         <input type="button" value = '9' onclick = "Solve('9')">
         <input type="button" value = 'x' onclick = "Solve('*')">
         <br>
         <input type="button" value = '4' onclick = "Solve('4')">
         <input type="button" value = '5' onclick = "Solve('5')">
         <input type="button" value = '6' onclick = "Solve('6')">
         <input type="button" value = '-' onclick = "Solve('-')">
         <br>
         <input type="button" value = '1' onclick = "Solve('1')">
         <input type="button" value = '2' onclick = "Solve('2')">
         <input type="button" value = '3' onclick = "Solve('3')">
         <input type="button" value = '+' onclick = "Solve('+')">
         <br>
         <input type="button" value = '00'onclick = "Solve('00')">
         <input type="button" value = '0' onclick = "Solve('0')">
         <input type="button" value = '.' onclick = "Solve('.')">
         <input type="button" value = '=' onclick = "Result()">
      </div>
   </div>
   <script src = 'Calc.js' ></script>
</body>
</html>
