<!DOCTYPE html>
<html>

<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Random number</title>
</head>

<body>

	<h1>Guess The Number Game</h1>
	Enter Your Name: <input type="text" name="Name" id="name"> 
	<button onclick="randomnum()">Start</button><br><br>
	<span style="display: none;" id="span">
	Guess the Numbar:<input type="text" id="Guessno">
	<button onclick="check()">Check</button>
    </span>
	<p id="result"></p>
	<p id="score"></p>
	<script>
		var res = document.getElementById("result");
		var Score = document.getElementById("score");
		var counts = 0;
		var ranum;
		
		function randomnum() {
			 ranum = Math.floor(Math.random() * 10) + 1;
			 document.getElementById("span").style.display="block";
		}
		function check() {
			var nam = document.getElementById("name").value;
			var predict = document.getElementById("Guessno").value;
			if (ranum == predict) {
				res.textContent = "You are right";
				alert(nam + " You won the Game💕 and you have tried "+ counts +" times");
			}
			else {
				counts = counts + 1;
				Score.textContent = "COUNT:" + " " + counts;
				res.textContent = "You are Wrong";
				// alert(nam + " You Lose the Game👎");
			}

		}
	</script>
</body>

</html>
