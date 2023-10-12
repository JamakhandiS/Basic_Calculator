# Basic_Calculator
------------------HTML CODE start----------------------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="utils.css">
    <link rel="stylesheet" href="style.css">
    <title>Basic calculator</title>
</head>
<body>
    <h2 class="text-container">Calculator</h2>
    <div class="container text-container " >
        <div class="row">
            <input class="input" type="text"/>
            <button class="button">AC</button>
        </div>
        <div class="row" >
            <button class="button">9</button>
            <button class="button">8</button>
            <button class="button">7</button>
            <button class="button">+</button>
        </div>
        <div class="row" >
            <button class="button">4</button>
            <button class="button">5</button>
            <button class="button">6</button>
            <button class="button">-</button>
        </div>
        <div class="row">
            <button class="button">1</button>
            <button class="button">2</button>
            <button class="button">3</button>
            <button class="button">/</button>
        </div>
        <div class="row">
            <button class="button">.</button>
            <button class="button">0</button>
            <button class="button">=</button>
            <button class="button">X</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

-----------------------HTML CODE END--------------------

------------------------CSS CODE START-------------------

***********style.css file***************
html body{
    height: 100%;
    width:100%;
}

.button{
    padding: 10px;
    margin: 1px 3px;
    border-radius:5px;
    border-width: 1px;
    height: 40px;
    width: 40px;
    font-size: 18px;
    font-style: inherit;
}
.row{
    margin:8px 0;
}
.row input{
    margin: 0;
    border: 2px solid;
    border-radius: 8px;
    padding: 4px 3px;
    font-size: 20px;
    width: 140px;
}

********util.css file***********


_-----------------------CSS code END------------------


-----------------------JS CODE START------------------
let string="";
let buttons= document.querySelectorAll('.button');
Array.from(buttons).forEach((button)=>{
    button.addEventListener('click',(e)=>{
        if(e.target.innerHTML == '='){
            string =eval(string);
            document.querySelector('input').value = string;
        }
        else if(e.target.innerHTML == 'AC'){
            string ="";
            document.querySelector('input').value = string;
        }
        else if(e.target.innerHTML == 'X'){
            string =e.target.innerHTML*e.target.innerHTML;
            document.querySelector('input').value = string;
        }
        else{
        console.log(e.target)
        string = string + e.target.innerHTML;
        document.querySelector('input').value = string;
        }
    })
})
--------------------JS code END----------------------------
