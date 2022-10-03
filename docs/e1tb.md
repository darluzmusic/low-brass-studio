<body onload="selectFunction()">
Exercises:
  <select id="mySelect" onchange="selectFunction()">
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

<p id="music"></p>

<script>
const aud_dir = "https://e1-assets.s3.us-west-1.amazonaws.com/";
const aud_name = "E1TB"
const aud_path = `${aud_dir}${aud_name}`;
const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
const img_name = "B1Tbn";
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
