
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> official Calculator</title>
    <style>
        **{
            background-color: aqua;
        }
        h3{
            color: red;
        }
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body{
            width: 100%;
            height: 70vh;
            display: grid;
            place-items: center;
        }
        .Calculator{
            margin: auto;
            padding: 20px;
            background-color: #f2f2f2;
            box-shadow: 0px 0px 5px #888888;
            width: 350px;
        }
        .display{
            margin-bottom: 10px;

        }
        input[type="text"]{
            width: 100%;
            height: 60px;
            font-size: 30px;
            text-align: right;
            padding-right: 5px;
            border: none;
            background-color: #fff;
        }

        .button{
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-gap: 5px;
        }
        button{
            height: 70px;
            font-size: 20px;
            background-color: #e6e6e6;
            border: none;
            cursor: pointer;
        }
        button:hover{
            background-color: #f2f2;
        }
        .eg{
            background-color: #fb7c14;
        }

    </style>
</head>
<body>
    <h3>CALCULATOR</h3>
    <div class="Calculator">
        <div class="display">
          <input type="text" id="result" disabled>
        </div>
        <div class="button">
            <button onclick="clearResult()">AC</button>
            <button onclick="deleteResult()">DEL</button>
            <button onclick="insertValue('%')">%</button>
            <button onclick="insertValue('/')">/</button>
            <button onclick="insertValue('7')">7</button>
            <button onclick="insertValue('8')">8</button>
            <button onclick="insertValue('9')">9</button>
            <button onclick="insertValue('*')">*</button>
            <button onclick="insertValue('4')">4</button>
            <button onclick="insertValue('5')">5</button>
            <button onclick="insertValue('6')">6</button>
            <button onclick="insertValue('-')">-</button>
            <button onclick="insertValue('1')">1</button>
            <button onclick="insertValue('2')">2</button>
            <button onclick="insertValue('3')">3</button>
            <button onclick="insertValue('+')">+</button>
            <button onclick="insertValue('00')">00</button>
            <button onclick="insertValue('0')">0</button>
            <button onclick="insertValue('.')">.</button>
            <button class="eg" onclick="Calculate()">=</button>
        </div>
    </div>
    <script>
        let Result = document.getElementById('result');

        function insertValue(value){
            Result.value +=value;
        }
        function clearResult(){
            Result.value = ' ';
        }            
        function deleteResult(){
            result.value = Result.value.slice(0,-1);
        }

        function Calculate(){
            try{
                Result.value = eval(Result.value);
            }
            catch(error){
                Result.value = "error";
            }
        }
    </script>
</body>
</html>
