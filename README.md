# Pizza_Project

This Pizza Project created a website that takes user input for a pizza order. Using HTML and CSS, the website presents a menu with three customizations to choose from: Size, Vegetables, Meats. The Size column is a button selector, and the two other columns are checkboxes. The user can select their pizza customizations and press the place order button. Using JavaScript, the ordered items will be listed along with the total price. 

Using HTML, the structure of the menu is formed. The menu is built with a column for each category - Pizza Size, Veggie Selection, Meat Selection: 

    <div class="menu left">
        <h3>Size:</h3>
        <input class="size" type="radio" name="Size"
            value="Personal Pizza">Personal Pizza<br>
        <input class="size" type="radio" name="Size"
        value="Small Pizza">Small Pizza<br>
        <input class="size" type="radio" name="Size"
            value="Medium Pizza">Medium Pizza<br>
        <input class="size" type="radio" name="Size"
            value="Large Pizza">Large Pizza<br>
        <input class="size" type="radio" name="Size"
            value="Extra Large Pizza">Extra Large Pizza<br>
    </div>

    <div class="menu center">
        <h3>Vegetables:</h3>
        <input class="toppings" type="checkbox" name="Topping"
            value="Mushrooms">Mushrooms<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Onions">Onions<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Tomatoes">Tomatoes<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Olives">Olives<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Green Peppers">Green Peppers<br>
    </div>

    <div class="menu right">
        <h3>Meats:</h3>
        <input class="toppings" type="checkbox" name="Topping"
            value="Pepperoni">Pepperoni<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Sausage">Sausage<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Candian Bacon">Candian Bacon<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Ground Beef">Ground Beef<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Anchovy">Anchovy<br>
        <input class="toppings" type="checkbox" name="Topping"
            value="Chicken">Chicken<br>
        <input class="toppings" type="checkbox" name="Topping"
        value="Salami">Salami<br>
    </div>
                
This HTML creates the sub-total cart: 

    <div id ="cart">
        <div id="showText"></div>
        <div id="totalPrice"></div>
    </div>  
                
This JS initializes our string so it can get passed from function to function, growing line by line into a full receipt

    function getReceipt() {
    var text1 = "<h3>You Ordered:</h3>";
    var runningTotal = 0;
    var sizeTotal = 0;
    var sizeArray = document.getElementsByClassName("size");
    for (var i=0; i<sizeArray.length; i++) {
        if (sizeArray[i].checked) {
            var selectedSize = sizeArray[i].value;
            text1 = text1+selectedSize+"<br>";
        }
    }


This JS adds each user selection and relays the total: 

    runningTotal = (runningTotal + toppingTotal);
    console.log("total selected topping items: "+toppingCount);
    console.log(toppingCount+" topping - 1 free topping = "+"$"+toppingTotal+".00");
    console.log("topping text1: "+text1);
    console.log("Purchase Total: "+"$"+runningTotal+".00");
    document.getElementById("showText").innerHTML=text1;
    document.getElementById("totalPrice").innerHTML = "</h3>Total: <strong>$"+
        runningTotal+".00"+"</strong></h3>";
        
![PPimage](/menu.PNG?raw=true "Optional Title")
