<head>
  <style>
    hr {
      height:10px;
      border-radius:25px;
      background-color:#75ab9a;
      border-style:none;
    }
    #audioControl {
      display: flex;
      align-items:center;
    }
    #numberSelect {
      display: flex;
      flex-wrap: wrap;
      align-content: space-between;
    }
    #numberButton {
      border-radius: 5px;
      background-color: #75ab9a;
      color: white;
      padding: 10px;
      margin: 0.2vw;
      text-decoration: none;
}
  </style>
</head>
<body onload="selectFunction()">
  <h1 id="top">ESSENTIAL ELEMENTS FOR BAND:</h1>
    <h2>TROMBONE BOOK 1</h2>
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
  <p id="numberSelect"></p>
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
  const aud_name = "E1TB"
  const aud_path = `${aud_dir}${aud_name}`;
  const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
  const img_name = "B1Tbn";
  const img_path = `${img_dir}${img_name}`;
  function audioRestart(id) {
        document.getElementById(id).currentTime=0;}
  function selectFunction() {
    let text1 = "";
    let text2 = "";
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
      var img = "<img id=exercise" + i + " width='100%' src=" + img_path + zero + i + ".jpg>";
      var aud = "<div id=audioControl><audio id=" + i + " controls><source src=" +  aud_path + i + ".mp3></audio><button onclick=audioRestart(" + i + ")>🔃</button></div>";
      text1 += img + aud + "<br><a href=#top>⬆️</a><br><hr>";
      text2 += "<a id=numberButton href=#exercise" + i + "> " + i + "</a>"
    }
    document.getElementById("music").innerHTML = text1;
    document.getElementById("numberSelect").innerHTML = text2;
  }
  </script>
  </body>
