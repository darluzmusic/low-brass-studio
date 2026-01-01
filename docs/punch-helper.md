<html>
<body>

<p>Punch Helper</p>

<input type="text" value="Juana Briones Elementary" id="myInput">
<button onclick="myFunction()">Copy text</button>
<input type="text" value="10:25am" id="myInput">
<button onclick="myFunction()">Copy text</button>
<input type="text" value="11:50am" id="myInput">
<button onclick="myFunction()">Copy text</button>

<script>
function myFunction() {
  // Get the text field
  var copyText = document.getElementById("myInput");

  // Select the text field
  copyText.select();
  copyText.setSelectionRange(0, 99999); // For mobile devices

  // Copy the text inside the text field
  navigator.clipboard.writeText(copyText.value);

}
</script>

</body>
</html>