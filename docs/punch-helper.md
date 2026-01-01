<html>
<body>

<p>Juana Briones</p>

<button onclick="myFunction('1')">Copy text</button><input type="text" value="10:25am" id="1"><br><br>

<button onclick="myFunction('2')">Copy text</button><input type="text" value="11:50am" id="2"><br><br>

<button onclick="myFunction('3')">Copy text</button><input type="text" value="Juana Briones" id="3"><br><br>

<p>Fairmeadow</p>

<button onclick="myFunction('4')">Copy text</button><input type="text" value="1:25pm" id="4"><br><br>

<button onclick="myFunction('5')">Copy text</button><input type="text" value="2:15pm" id="5"><br><br>

<button onclick="myFunction('6')">Copy text</button><input type="text" value="Fairmeadow" id="6"><br><br>

<script>
function myFunction(id) {
  // Get the text field
  var copyText = document.getElementById(id);
  navigator.clipboard.writeText(copyText.value);
  
}
</script>

</body>
</html>
