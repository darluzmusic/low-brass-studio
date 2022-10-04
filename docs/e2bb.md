<h1>ESSENTIAL ELEMENTS FOR BAND:</h1>
  <h2>BARITONE BOOK 2</h2>
<body onload="selectFunction()">
Exercises:
  <select id="mySelect" onchange="selectFunction()">
  <option>1-10</option>
  <option>11-19</option>
  <option>20-31</option>
  <option>32-43</option>
  <option>44-55</option>
  <option>56-62</option>
  <option>63-74</option>
  <option>75-86</option>
  <option>87-99</option>
  <option>100-106</option>
  <option>107-115</option>
  <option>116-126</option>
  <option>127-133</option>
  <option>134-143</option>
  <option>144-150</option>
  <option>151-153</option>
   <optgroup label="Chorales">
  <option>154-158</option>
    </optgroup>
    <optgroup label="Major Scales">
  <option>159-162</option>
  <option>163-166</option>
  <option>167-170</option>
  <option>171-174</option>
  <option>175-178</option>
    </optgroup>
    <optgroup label="G, C, D Minor Scales">
  <option>179-184</option>
    </optgroup>
    <optgroup label="Chromatic Scales">
  <option>185-186</option>
    </optgroup>
    <optgroup label="Individual Study">
  <option>187-198</option>
   </optgroup>
    <optgroup label="Solo">
  <option>199-200</option>
    </optgroup>
</select>

<p id="music"></p>

<script>
const aud_dir = "https://e2-assets.s3.us-west-1.amazonaws.com/";
const aud_name = "E2BB"
const aud_path = `${aud_dir}${aud_name}`;
const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
const img_name = "B2BarBC2";
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
    text +="<img src=" + img_path + zero + i + ".jpg><br><audio controls><source src=" +  aud_path + i + ".mp3></audio><br><hr>";
  }
  document.getElementById("music").innerHTML = text;
}
</script>
</body>
