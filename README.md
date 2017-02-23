# Primes-
Prime factorization
//Code below

<!doctype html>
<html>
  <head>
    <link type= "text/css">
  <script language="javascript"></script>
        <title>Prime Factorization</title>
          <meta charset=“UTF-8”>
          <style>

            body {
              margin: 0;
              background: linear-gradient(to right, #39adff , purple);
              font-family: Arial;
              font-size: 24px;
              color: white;
            }

            h1 {
              text-align: center;
              font-size: 40px;
              padding-top: 50px;
            }

            p {
              text-align: center;
              padding-top: 125px;
              font-size: 18px;

            }

            .wrapper {
              text-align: center;
              padding: 25px;
              margin: 0px 475px 0px 475px;
              border-style: solid;
              border-color: inherit;
              border-radius: 5px;

            }

            .button {
              background-color: inherit;
              top: 50%;
              font-size: 16px;
              border-style: solid;
              border-radius: 5px;
              border-color: white;
              color: white;
              cursor: pointer;
            }

            a:hover {
              background-color: #39adff;
            }

            #answer {
              padding-top: 0px;
            }

          </style>
        </head>
<body>
<h1> Prime Factorization Program </h1>
<script>

function factorise(){ // assign the algorithm
  var n = document.getElementById("input").value; // sets up the variable to be used later
  var factors = new Array; // define variable factors as a new array
  for (var i = 2; i <= n; i++){ //start loop at 2, loop tops when variable i is less than or greater than n, count by 1 incrementally
    while (n % i == 0) { //while loop n modulo i equals 0,
      n = n/i;          //if true, check if n is divisible by i
      factors.push(i);  //if true, push into array, it's a prime factor to n
    }
  }
  // output in console
  console.log(factors);

  // output in popup
  alert('The prime factors of ' + n + ' are: ' + factors);

  //outputs the value on the page after the popup
  document.getElementById("answer").innerHTML = 'The prime factors of ' + n + ' are: ' + factors;

  return factors;
}
</script>

<div>
<p>Click The Button To Begin Prime Factoring</p>
</div>


<div class="wrapper">
  <input id="input" type="number" name="integer" value="0">
<br>
    <button class="button" onclick ="factorise();">Let's Factor!</button>
<p id="answer"></p>
</div>



</body>
</html>
