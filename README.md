<!DOCTYPE html>
<html>
<head>
  <meta charset = "utf-8">
  <title>Mini calculator</title>
 </head>
 <body> 
  <h1 style="text-align:center">LETS CALCULATE!</h1>
  <center>
  <h1>Area and Perimeter of Rectangle</h1>
        <h2 id="area"></h2>
        <h2 id="perimeter"></h2>
        <label for="len">Length:
            <input type="text" id="len">
        </label>
        <label for="wid">Width:
            <input type="text" id="wid">
        </label>
        <button id="calcBtn">Calculate</button>
        <br>
        <form name=form1>
        <br>
        <h1>Area and circumferance of the circle</h1>
        Enter the radius of circle:
       <input type="text" name="txtRadius" size=10>
       <input type="button" value="Calculate" onClick='CalculateArea();'> 
       </form> 
   
    <h2> Prime Numbers</h2>
      Enter the Limit of Number:
        <input type="number" name="limit" id="limit" min="0" style="width: 100px;">
        <input type="submit" value="Show" onclick="printPrime()" name="print">
        <div id="result">
        </div>
      </center>
  <script type="text/javascript">
    function CalculateArea(){
        var radius =document.form1.txtRadius.value;
        document.write("<P>The area of the circle is " + (radius * radius * Math.PI) + "</p>");
        document.write("<P>The circumference of the circle is " + (2 * radius * Math.PI) + "</p>");
    }

            var lenEl=document.querySelector("#len");
            var widEl=document.querySelector("#wid");
            
            var calcBtn=document.querySelector("#calcBtn");
            
            var areagEl=document.querySelector("#area");
            var perimeterEl=document.querySelector("#perimeter");
            
            
            calcBtn.onclick=function(){
                
              
                area=Number(lenEl.value)*Number(widEl.value)
                
              
                perimeter=2*(Number(lenEl.value)+Number(widEl.value))
 
                
            
                areagEl.innerHTML="Area of rectange:"+area;
                perimeterEl.innerHTML="Perimeter of rectange:"+perimeter;
            }
           function printPrime() {
                var i = 0;
                var j = 0;
 
                limit = document.getElementById('limit').value;
 
               
                for (i = 1; i <= limit; i++) {
                    c = 0;
 
                    for (j = 1; j <= i; j++) {
                        
                        if (i % j == 0) {
                  
                            c++;
                        }
                    }
 
                    if (c == 2) {
                        document.getElementById("result").insertAdjacentHTML('beforeend', i + '<br>');
                    }
                }
            }
    </script>
 </body> 
</html>
