<h1>ESSENTIAL ELEMENTS FOR BAND:</h1>
  <h2>BARITONE BOOK 1</h2>
<body onload="selectFunction()">
Exercises:
  <select id="exerciseSelect" onchange="selectFunction()">
  <option>1-13</option>
  <option>14-26</option>
  <option>27-39</option>
  <option>40-51</option>
  <option>52-58</option>
  <option>59-72</option>
  <option>73-85</option>
  <option>86-99</option>
  <option>100-109</option>
  <option>110-118</option>
  <option>119-131</option>
  <option>132-146</option>
  <option>147-153</option>
  <option>154-164</option>
  <option>165-174</option>
  <option>175-181</option>
  <option>182-184</option>
  <option>185-187</option>
</select>
      <button onclick="exercise_previous(); selectFunction();">⬅️</button>
      <button onclick="exercise_next(); selectFunction();">➡️</button>
    <br>
<p id="music"></p>

<script>
  //BUTTONS//
    function exercise_previous() {
        var x = 
    document.getElementById("exerciseSelect").selectedIndex;
    document.getElementById("exerciseSelect").selectedIndex = x - 1;
    }
    function exercise_next() {
        var x = 
    document.getElementById("exerciseSelect").selectedIndex;
    document.getElementById("exerciseSelect").selectedIndex = x + 1;
    }
const aud_dir = "https://e1-assets.s3.us-west-1.amazonaws.com/";
const aud_name = "E1BB"
const aud_path = `${aud_dir}${aud_name}`;
const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
const img_name = "B1BarBC";
const img_path = `${img_dir}${img_name}`;
function selectFunction() {
  let text = "";
  var x = document.getElementById("exerciseSelect").value;
  const myArray = x.split("-");
  var i = myArray[0];
  var num = myArray[1];
  for (; i <= num; i++) 
  {
    if (i < 10) {
    zero = "00";
  } else if (i < 100) {
    zero = "0";
  } else {
    zero = "";
  }
    text +="<img width='100%' src=" + img_path + zero + i + ".jpg><br><audio controls><source src=" +  aud_path + i + ".mp3></audio><br><hr style='height:10px;border-radius:25px;background-color:#75ab9a;border-style:none;'>";
  }
  document.getElementById("music").innerHTML = text;
}
</script>
</body>
