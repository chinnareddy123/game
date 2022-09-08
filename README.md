# game
GEEKSFORGEEKS
Building a Dice Game using JavaScript
We will be building a Dice Game Project using HTML, CSS, and JavaScript. The Dice Game is based on a two-player. Both players roll the dice and the player who gets the highest phase value will win the game.

Images of Dice Phases: The list of dice phases images are given below. Save all the images in a folder where you save your HTML, CSS, and JavaScript files. You can save all HTML, CSS, and JavaScript files separately and link CSS and JavaScript files to the HTML file or combine all codes (HTML, CSS and JavaScript) in a single file and execute it.

Dice 1
Dice 2
Dice 3
Dice 4
Dice 5
Dice 6
HTML Code: HTML code is used to design the basic structure of the project. The HTML code contains the container class that holds the player’s name and initial dice phase. Another bottom div contains the two buttons (one button for roll the dice and another button for rename the player name).

<!DOCTYPE html> 

<html lang="en"> 

  

<head> 

    <meta charset="UTF-8"> 

    <meta name="viewport" content= 

        "width=device-width, initial-scale=1.0"> 

    <title>Dice Game</title> 

</head> 

  

<body> 

    <div class="container"> 

        <h1>Let's Play</h1> 

  

        <div class="dice"> 

            <p class="Player1">Player 1</p> 

            <img class="img1" src="dice6.png"> 

        </div> 

  

        <div class="dice"> 

            <p class="Player2">Player 2</p> 

            <img class="img2" src="dice6.png"> 

        </div> 

    </div> 

  

    <div class="container bottom"> 

        <button type="button" class="butn"

            onClick="rollTheDice()"> 

            Roll the Dice 

        </button> 

    </div> 

    <div class="container bottom"> 

        <button type="button" class="butn" 

            onClick="editNames()"> 

            Edit Names 

        </button> 

    </div> 

</body> 

  

</html> 
CSS Code: In this section, we will use some CSS property to style the Dice Game.

<style> 

    .container { 

        width: 70%; 

        margin: auto; 

        text-align: center; 

    } 

  

    .dice { 

        text-align: center; 

        display: inline-block; 

        margin: 10px; 

    } 

  

    body { 

        background-color: #042f4b; 

        margin: 0; 

    } 

  

    h1 { 

        margin: 30px; 

        font-family: "Lobster", cursive; 

        text-shadow: 5px 0 #232931; 

        font-size: 4.5rem; 

        color: #4ecca3; 

        text-align: center; 

    } 

  

    p { 

        font-size: 2rem; 

        color: #4ecca3; 

        font-family: "Indie Flower", cursive; 

    } 

  

    img { 

        width: 100%; 

    } 

  

    .bottom { 

        padding-top: 30px; 

    } 

  

    .butn { 

        background: #4ecca3; 

        font-family: "Indie Flower", cursive; 

        border-radius: 7px; 

        color: #ffff; 

        font-size: 30px; 

        padding: 16px 25px 16px 25px; 

        text-decoration: none; 

    } 

  

    .butn:hover { 

        background: #232931; 

        text-decoration: none; 

    } 
</style> 
JavaScript Code: The JavaScript code contains the functionality of Dice Game. The first functionality is to rename the player name after clicking the button. Another functionality is to roll the dice after clicking the button. After rolling the dice by both the player, anyone player will win who get the highest phase value. If both players get the same phase value then the game will draw.

<script> 

  

    // Player name 

    var player1 = "Player 1"; 

    var player2 = "Player 2"; 

  

    // Function to change the player name 

    function editNames() { 

        player1 = prompt("Change Player1 name"); 

        player2 = prompt("Change player2 name"); 

  

        document.querySelector("p.Player1").innerHTML = player1; 

        document.querySelector("p.Player2").innerHTML = player2; 

    } 

  

    // Function to roll the dice 

    function rollTheDice() { 

        setTimeout(function () { 

            var randomNumber1 = Math.floor(Math.random() * 6) + 1; 

            var randomNumber2 = Math.floor(Math.random() * 6) + 1; 

  

            document.querySelector(".img1").setAttribute("src", 

                "dice" + randomNumber1 + ".png"); 

  

            document.querySelector(".img2").setAttribute("src", 

                "dice" + randomNumber2 + ".png"); 

  

            if (randomNumber1 === randomNumber2) { 

                document.querySelector("h1").innerHTML = "Draw!"; 

            } 

  

            else if (randomNumber1 < randomNumber2) { 

                document.querySelector("h1").innerHTML 

                                = (player2 + " WINS!"); 

            } 

  

            else { 

                document.querySelector("h1").innerHTML 

                                = (player1 + " WINS!"); 

            } 

        }, 2500); 

    } 
</script> 
Complete Code: After combining the above three sections (HTML, CSS, and JavaScript) code, we will get the complete Dice Game.

<!DOCTYPE html> 

<html lang="en"> 

  

<head> 

    <meta charset="UTF-8"> 

    <meta name="viewport" content

        ="width=device-width, initial-scale=1.0"> 

    <title>Dice Game</title> 

  

    <style> 

        .container { 

            width: 70%; 

            margin: auto; 

            text-align: center; 

        } 

  

        .dice { 

            text-align: center; 

            display: inline-block; 

            margin: 10px; 

        } 

  

        body { 

            background-color: #042f4b; 

            margin: 0; 

        } 

  

        h1 { 

            margin: 30px; 

            font-family: "Lobster", cursive; 

            text-shadow: 5px 0 #232931; 

            font-size: 4.5rem; 

            color: #4ecca3; 

            text-align: center; 

        } 

  

        p { 

            font-size: 2rem; 

            color: #4ecca3; 

            font-family: "Indie Flower", cursive; 

        } 

  

        img { 

            width: 100%; 

        } 

  

        .bottom { 

            padding-top: 30px; 

        } 

  

        .butn { 

            background: #4ecca3; 

            font-family: "Indie Flower", cursive; 

            border-radius: 7px; 

            color: #ffff; 

            font-size: 30px; 

            padding: 16px 25px 16px 25px; 

            text-decoration: none; 

        } 

  

        .butn:hover { 

            background: #232931; 

            text-decoration: none; 

        } 

    </style> 

</head> 

  

<body> 

    <div class="container"> 

        <h1>Let's Play</h1> 

  

        <div class="dice"> 

            <p class="Player1">Player 1</p> 

            <img class="img1" src="dice6.png"> 

        </div> 

  

        <div class="dice"> 

            <p class="Player2">Player 2</p> 

            <img class="img2" src="dice6.png"> 

        </div> 

    </div> 

  

    <div class="container bottom"> 

        <button type="button" class="butn"

            onClick="rollTheDice()"> 

            Roll the Dice 

        </button> 

    </div> 

    <div class="container bottom"> 

        <button type="button" class="butn"

            onClick="editNames()"> 

            Edit Names 

        </button> 

    </div> 

  

    <script> 

  

        // Player name 

        var player1 = "Player 1"; 

        var player2 = "Player 2"; 

  

        // Function to change the player name 

        function editNames() { 

            player1 = prompt("Change Player1 name"); 

            player2 = prompt("Change player2 name"); 

  

            document.querySelector("p.Player1") 

                            .innerHTML = player1; 

                              

            document.querySelector("p.Player2") 

                            .innerHTML = player2; 

        } 

  

        // Function to roll the dice 

        function rollTheDice() { 

            setTimeout(function () { 

                var randomNumber1 = Math.floor(Math.random() * 6) + 1; 

                var randomNumber2 = Math.floor(Math.random() * 6) + 1; 

  

                document.querySelector(".img1").setAttribute("src", 

                    "dice" + randomNumber1 + ".png"); 

  

                document.querySelector(".img2").setAttribute("src", 

                    "dice" + randomNumber2 + ".png"); 

  

                if (randomNumber1 === randomNumber2) { 

                    document.querySelector("h1").innerHTML = "Draw!"; 

                } 

  

                else if (randomNumber1 < randomNumber2) { 

                    document.querySelector("h1").innerHTML 

                        = (player2 + " WINS!"); 

                } 

  

                else { 

                    document.querySelector("h1").innerHTML 

                        = (player1 + " WINS!"); 

                } 

            }, 2500); 

        } 

    </script> 

</body> 

  

</html> 







