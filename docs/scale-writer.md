<html>
<body>

<h2>Scale Writer</h2>
<select id="rootSelect">
    <option value="2,5,8,11,14,17,20,23,26">C♯</option>
    <option value="11,14,17,19,23,26,29,32,35">F♯</option>
    <option value="19,23,26,28,32,35,38,40,44">B</option>
    <option value="7,11,14,16,19,23,26,28,32">E</option>
    <option value="16,19,23,25,28,32,35,37,40">A</option>
    <option value="4,7,11,13,16,19,23,25,28">D</option>
    <option value="13,16,19,22,25,28,32,34,37">G</option>
    <option value="1,4,7,10,13,16,19,22,25" selected>C</option>
    <option value="10,13,16,18,22,25,28,31,34">F</option>
    <option value="18,22,25,27,31,34,37,39,43">B♭</option>
    <option value="6,10,13,15,18,22,25,27,31">E♭</option>
    <option value="15,18,22,24,27,31,34,36,39">A♭</option>
    <option value="3,6,10,12,15,18,22,24,27">D♭</option>
    <option value="12,15,18,21,24,27,31,33,36">G♭</option>
    <option value="0,3,6,9,12,15,18,21,24">C♭</option>
  </select>
  <select id="chordSelect">
    <option value="0,0,0,0,0,0,0,0,0">maj7</option>
    <option value="0,0,0,0,0,0,1,0,0">7</option>
    <option value="0,0,1,0,0,0,1,0,0">-7</option>
    <option value="0,1,1,0,1,1,1,0,1">-7b5</option>
  </select>
<button onclick="myFunction()">Click me</button>
<p id="demo"></p>

<script>
function myFunction() {
const noteArray = ["C♭",	"C",	"C♯",	"D♭",	"D",	"D♯",	"E♭",	"E",	"E♯",	"F♭",	"F",	"F♯",	"G♭",	"G",	"G♯",	"A♭",	"A",	"A♯",	"B♭",	"B",	"B♯",	"C♭",	"C",	"C♯",	"D♭",	"D",	"D♯",	"E♭",	"E",	"E♯",	"F♭",	"F",	"F♯",	"G♭",	"G",	"G♯",	"A♭",	"A",	"A♯",	"B♭",	"B",	"B♯",	"C♭",	"C",	"C♯"
];
var x = document.getElementById("rootSelect").value;
const keyArray = x.split(",");
var y = document.getElementById("chordSelect").value;
const chordArray = y.split(",");
let scale = "";
for (let i = 0; i <= 8; i++) {
    scale += noteArray[keyArray[i]-chordArray[i]] + " ";
}
document.getElementById("demo").innerHTML = scale;
}
</script>

</body>
</html>
