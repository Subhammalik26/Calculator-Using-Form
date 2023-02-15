# Calculator-Using-Form


# CODE :

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Calculator Using Form</title> <!-- Show the title of the web page-->
    <!-- Begins the javascript code-->
	<script type="text/javascript">
    // Seperate functions for all operations
		function add()
		{
			var a=eval(document.m1.t1.value);  // Declaring the 1st variable which stores & evaluates the First Value. 
			var b=eval(document.m1.t2.value); // Declaring the 2nd variable which stores & evaluates the 2nd Value. 
			var c=a+b;          // Declaring the 3rd variable which makes the operation between 1st and 2nd variables.
			document.m1.t3.value=c;  // storing the result value of 3rd variable in the class m1.
		}

		function sub()
		{
			var a=eval(document.m1.t1.value);
			var b=eval(document.m1.t2.value);
			var c=a-b;
			document.m1.t3.value=c;
		}
              
        function mul()
		{
			var a=eval(document.m1.t1.value);
			var b=eval(document.m1.t2.value);
			var	c=a*b;
			document.m1.t3.value=c;
		}

		function div()
		{
			var a=eval(document.m1.t1.value);
			var b=eval(document.m1.t2.value);
			var c=a/b;
			document.m1.t3.value=c;
			// Error Handling for invalid input using try...catch...throw block
			try {
            if (b == 0)
            {
              throw new Error('Cannot divide by zero'); // User-defined throw statement.
            }
                }
            catch (e) {
                document.m1.t3.value=e.message; // This will generate an error message.
                      }
		}
	</script>
</head>
<body>
	<form method="POST" name="m1" class="m1">  <!-- Creating input forms declaring a class in html-->
		<br>
		<h2 align="left"> Calculator </h2> <!-- Heading -->
		
				 <!-- Creating 2 input forms which will take take input from the user -->
                  
                    First Number: &nbsp&nbsp&nbsp &nbsp      
				    <input type="text" name="t1"/><br>
				    <br>
				    Second Number: &nbsp
					<input type="text" name="t2"/><br>
				    <br>
				<!-- Creating result form which displays the final result of any operation -->
				        
				    <input type="button" name="t3" value="Answer"/><br><br>
				<!-- Creating button of different operation and creating onClick event which executes 
					the certain operation when button is clicked -->
					<input type="button" name="t5" value="Addition" ="add()" /> <!--Function call of certain operation-->
					<input type="button" name="t6" value="Substraction" onclick="sub()" />
					<input type="button" name="t4" value="Multiplication" onclick="mul()" />
                    <input type="button" name="t7" value="Division" onclick="div()" />

						
	</form>
</body>
</html>

# OUTPUT SCREENSHOTS :

![output](https://user-images.githubusercontent.com/99710364/218970414-9555d701-5229-4c69-93cf-8501787072ff.png)

![error_handling_output](https://user-images.githubusercontent.com/99710364/218970420-a208acfb-aa36-41e3-9bbe-063ca4504581.png)



