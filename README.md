# Calculator App

simple calculator app with js and css

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="main">
        <form name="form">
            <input type="text" name="textview" class="textview">
            <table>
                <tr>
                    <td><input class="button button-clr"type="button" onclick="clean()" value="C"></td>
                    <td><input class="button button-bksp"type="button"onclick="backspace()" value="<"></td>
                    <td><input class="button button-op"type="button"onclick="insert('/')" value="/"></td>
                    <td><input class="button button-op"type="button"onclick="insert('*')" value="*"></td>
                </tr>
                <tr>
                    <td><input class="button button-in"type="button"onclick="insert(7)" value="7"></td>
                    <td><input class="button button-in"type="button"onclick="insert(8)" value="8"></td>
                    <td><input class="button button-in"type="button"onclick="insert(9)" value="9"></td>
                    <td><input class="button button-op"type="button"onclick="insert('+')" value="+"></td>
                </tr>
                <tr>
                    <td><input class="button button-in"type="button"onclick="insert(4)" value="4"></td>
                    <td><input class="button button-in"type="button"onclick="insert(5)" value="5"></td>
                    <td><input class="button button-in"type="button"onclick="insert(6)" value="6"></td>
                    <td><input class="button button-op"type="button"onclick="insert('-')" value="-"></td>
                </tr>
                <tr>
                    <td><input class="button button-in"type="button"onclick="insert(1)" value="1"></td>
                    <td><input class="button button-in"type="button"onclick="insert(2)" value="2"></td>
                    <td><input class="button button-in"type="button"onclick="insert(3)" value="3"></td>
                    <td rowspan="2"><input style="height: 108px"onclick="equal()" class="button button-eq"type="button" value="="></td>
                </tr>
                <tr>
                    <td colspan="2"><input style="width: 108px"onclick="insert(0)" class="button button-in"type="button" value="0"></td>
                    <td><input  class="button button-dot"type="button"onclick="insert('.')" value="."></td>
                    
                </tr>
            </table>
        </form>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
## CSS
```css
*{
    margin: 0;
    padding: 0;
}
.button{
    width: 50px;
    height: 50px;
    font-size: 25px;
    margin: 2px;
}
.textview{
    width: 208px;
    height: 30px;
    font-size: 25px;
    padding: 5px;
    border: none;
    border-radius: 10px;
    border: 1px solid black;
    margin: 4.7px;
    background-color: rgb(245, 244, 244);
}
.textview:hover{
    background-color: rgb(99, 99, 99);
    color: white;
}
form{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    background-color: rgb(4, 61, 83);
    padding: 10px;
    border-radius: 10px;
}
.button{
    border: 1px solid black;
    border-radius: 10px;
    color: white;
    cursor: pointer;
}
.button:hover{
    background-color: rgb(59, 59, 59);
    
}
.button-clr{
    background-color: rgb(250, 67, 67);
}
.button-bksp{
    background-color: rgb(250, 140, 67);
}
.button-op{
    background-color: rgb(67, 168, 250);
}
.button-eq{
    background-color: rgb(168, 67, 250);
}
.button-in{
    background-color: rgb(102, 151, 145);
}
.button-dot{
    background-color: rgb(206, 177, 49);
}
```

##  JavaScript
```js
function insert(num){
    document.form.textview.value=document.form.textview.value+num;
}
function clean(){
    document.form.textview.value="";
}
function equal(){
    document.form.textview.value=eval(document.form.textview.value);
}
function backspace(){
    var exp=document.form.textview.value;
    document.form.textview.value=exp.substring(0,exp.length-1);
}

```
