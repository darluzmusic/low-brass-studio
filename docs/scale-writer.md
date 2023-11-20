<html>
<style>
  #scale {
    padding-left: 5px;
  }
</style>
<body>
<h2>Scale Writer</h2>
<select id="rootSelect">
<option value="2,7,12,17,22,27,32,37,43">C♯</option>
<option value="17,22,27,31,37,43,49,54,59">F♯</option>
<option value="31,37,43,48,54,59,65,70,76">B</option>
<option value="11,17,22,26,31,37,43,48,54">E</option>
<option value="26,31,37,42,48,54,59,64,70">A</option>
<option value="6,11,17,21,26,31,37,42,48">D</option>
<option value="21,26,31,36,42,48,54,58,64">G</option>
<option value="1,6,11,16,21,26,31,36,42" selected>C</option>
<option value="16,21,26,30,36,42,48,53,58">F</option>
<option value="30,36,42,47,53,58,64,69,75">B♭</option>
<option value="10,16,21,25,30,36,42,47,53">E♭</option>
<option value="25,30,36,41,47,53,58,63,69">A♭</option>
<option value="5,10,16,20,25,30,36,41,47">D♭</option>
<option value="20,25,30,35,41,47,53,57,63">G♭</option>
<option value="0,5,10,15,20,25,30,35,41">C♭</option>
  </select>
  <select id="chordSelect">
    <option value="0,0,0,0,0,0,0,0,0">△, maj7, 6 | Major</option>
    <option value="0,0,0,0,0,0,1,0,0">7 | Mixolydian</option>
    <option value="0,0,1,0,0,0,1,0,0">-7 | Dorian</option>
    <option value="0,0,0,-1,0,0,0,0,0">maj+4 | Lydian</option>
    <option value="0,1,1,0,1,1,1,0,1">∅7, -7♭5 | Locrian</option>
    <option value="0,0,1,0,1,1,2,1,2">°7 | Diminished</option>
    <option value="0,0,0,-1,-1,-1,1,0,0">7+, 7aug | Whole Tone</option>
    <option value="0,0,0,-1,0,0,1,0,0">7♯11 | Lydian Dominant</option>
    <option value="0,1,0,0,0,1,1,0,-1">7♭9 | 3rd Mode of Bebop (Major)</option>
    <option value="0,1,0,-1,-1,1,1,0,-1">7♯9 | Diminished Whole Tone</option>
  </select><br>
<button onclick="scaleFunction()">Add Scale</button>
<button onclick="myBarline()">Add |</button>
<button onclick="myBarlinedbl()">Add ||</button>
<button onclick="myRepeatbar()">Add %</button>
<button onclick="clearFunction()">Clear</button>
<button onclick="editFunction()">Edit</button>
<button onclick="copyAll()">Copy All</button><br>
<div id="scale" contenteditable="true"></div>
<script>
function copyAll() {
  alert("Copied!");
  const richTextDiv = document.getElementById("scale");

const clipboardItem = new ClipboardItem({
	"text/plain": new Blob(
		[richTextDiv.innerText],
		{ type: "text/plain" }
	),
	"text/html": new Blob(
		[richTextDiv.outerHTML],
		{ type: "text/html" }
	),
});

navigator.clipboard.write([clipboardItem]);
}
function editFunction() {
  document.getElementById("scale").focus();
}
function clearFunction() {
  let text;
  if (confirm("Are you sure?") == true) {
    document.getElementById("scale").innerHTML = "";
  }
}
function myBarline() {
  const div = document.getElementById("scale");
div.insertAdjacentHTML('beforeend',"–––––––––––––––––––" + "<br>");
}
function myBarlinedbl() {
  const div = document.getElementById("scale");
div.insertAdjacentHTML('beforeend',"=================" + "<br>");
}
function myRepeatbar() {
  const div = document.getElementById("scale");
div.insertAdjacentHTML('beforeend',"                %" + "<br>");
}
function scaleFunction() {
let a = rootSelect.options[rootSelect.selectedIndex].text;
let b = chordSelect.options[chordSelect.selectedIndex].text;
const noteArray = ["C♭","C","C♯","D","C","D♭","D","D♯","E","D","E♭","E","E♯","F♯","E♭","F♭","F","F♯","G","F","G♭","G","G♯","A","G","A♭","A","A♯","B","A","B♭","B","B♯","C♯","B♭","C♭","C","C♯","D","C♭","C","D♭","D","D♯","E","D♭","D","E♭","E","E♯","F♯","E♭","F♭","F","F♯","G","F","G♭","G","G♯","A","G♭","G","A♭","A","A♯","B","A♭","A","B♭","B","B♯","C♯","B♭","C♭","C","C♯","D"
];
var x = document.getElementById("rootSelect").value;
const keyArray = x.split(",");
var y = document.getElementById("chordSelect").value;
const chordArray = y.split(",");
let scale = "<b>" + a + b + "</b>"+ "<br>";
for (let i = 0; i <= 8; i++) {
    scale += noteArray[keyArray[i]-chordArray[i]] + " ";
}
const div = document.getElementById("scale");
div.insertAdjacentHTML('beforeend', scale + "<br>");
}
</script>

</body>
</html>
