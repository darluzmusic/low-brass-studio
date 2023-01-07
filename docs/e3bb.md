<body onload="selectFunction()">
<h1>ESSENTIAL ELEMENTS FOR BAND:</h1>
  <h2>BARITONE BOOK 3</h2>
  Exercises:
  <select id="mySelect" onchange="selectFunction()">
  <option>1-11</option>
  <option>12-22</option>
  <option>23-34</option>
  <option>35-43</option>
  <option>44-55</option>
  <option>56-64</option>
  <option>65-73</option>
  <option>74-83</option>
  <option>84-92</option>
  <option>93-99</option>
  <option>100-111</option>
  <option>112-117</option>
  <option>118-127</option>
  <option>128-138</option>
  <option>139-148</option>
   <optgroup label="Individual Study"> 
  <option>149-157</option>
   </optgroup>
   <optgroup label="Reading Skill Builder"> 
  <option>158-166</option>
   </optgroup>
      <optgroup label="Chorales"> 
  <option>167-173</option>
   </optgroup>
      <optgroup label="The Basics of Jazz Style"> 
  <option>174-181</option>
   </optgroup>
      <optgroup label="Scales And Arpeggios"> 
  <option>182-195</option>
   </optgroup>
</select>
      <button onclick="exercise_previous(); selectFunction(); ">⬅️</button>
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
const aud_dir = "https://e3-assets.s3.us-west-1.amazonaws.com/";
const aud_name = "E3BB"
const aud_path = `${aud_dir}${aud_name}`;
const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
const img_name = "B3BarBC3";
const img_path = `${img_dir}${img_name}`;
function selectFunction() {
  let text = "";
  var x = document.getElementById("mySelect").value;
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
