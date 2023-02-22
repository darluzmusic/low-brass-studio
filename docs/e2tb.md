  <head>
    <title>E2TB</title>
  <style>
    select {
      color: white;
      background-color: gray;
      font-family: arial;
      font-size: 2rem;
      border-radius: 0.5rem;
      height: 4.5rem;
      text-align: center;
      margin: 0.1rem;
    }
    #top {
      padding-bottom: 0.5rem;
      font-family: arial;
      font-size: 3rem;
      color: #75ab9a;
    }
    #exercises {
      display:flex;
      align-items: center;
      padding-bottom: 0.5rem;
      font-family: arial;
      font-size: 3rem;
    }
    #numberSelect {
      display: flex;
      flex-wrap: wrap;
      align-content: space-between;
      padding-bottom: 0.5rem;
    }
    #numberButton {
      font-family:Arial, Helvetica, sans-serif;
      font-size: 2rem;
      border-radius: 0.5rem;
      background-color: #75ab9a;
      color: white;
      padding: 1rem;
      margin: 0.1rem;
      text-decoration: none;
    }
    #transport {
      display: flex;
      align-items:center;
      flex-wrap: wrap;
    }
    #audioControl {
      display: flex;
      flex-wrap: wrap;
      align-items:center;
      margin-right:3rem;
    }
    #nav {
      display: flex;
    }
    #navButton {
      cursor: pointer;
      font-size: 2rem;
      border-radius: 0.5rem;
      background-color: #75ab9a;
      color: white;
      padding: 1rem;
      margin: 0.1rem;
      text-decoration: none;
    }
    #pad {
      height: 1440px;
    }
  </style>
</head>
<body onload="selectFunction()">
  <div id="top" style="font-family:Arial, Helvetica, sans-serif">ESSENTIAL ELEMENTS FOR BAND:<br>TROMBONE BOOK 2</div>
    <div id="exercises">
    <select id="exerciseSelect" onchange="selectFunction()">
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
    <option>187-200</option>
    </optgroup>
    <optgroup label="Solo">
    <option>201-202</option>
    </optgroup>
    </select>
    <div id="navButton" onclick="pagePrevious(); selectFunction();">⬅️</div>
    <div id="navButton" onclick="pageNext(); selectFunction();">➡️</div>
    </div>
      <br>
  <div id="numberSelect"></div>
  <hr style="height:1rem;
  border-radius:0.5rem;
  background-color:#75ab9a;
  border-style:none;">
  <div id="music"></div>
  <div id="pad"></div>

  <script>
    //BUTTONS//
    function pagePrevious() {
      var x = 
      document.getElementById("exerciseSelect").selectedIndex;
      document.getElementById("exerciseSelect").selectedIndex = x - 1;
      }
    function pageNext() {
      var x = 
      document.getElementById("exerciseSelect").selectedIndex;
      document.getElementById("exerciseSelect").selectedIndex = x + 1;
      }
    //RESTART//
    function audioRestart(id) {
      var y = document.getElementById(id);   
      y.currentTime=0;
      y.pause();
      }
    //PLAYBACKRATE//
    //Needed '' in function call to read as id//
    function audioRate(l,m) {
      var r = document.getElementById(l);
      var v = document.getElementById(m).value;
      r.playbackRate = v;
    }
    //LOOP//
    const aud_dir = "https://e2-assets.s3.us-west-1.amazonaws.com/";
    const aud_name = "E2TB"
    const aud_path = `${aud_dir}${aud_name}`;
    const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
    const img_name = "B2Tbn2";
    const img_path = `${img_dir}${img_name}`;

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
        var aud = "<audio id=" + i + " controls><source src=" +  aud_path + i + ".mp3></audio><a id=navButton onclick=audioRestart(" + i + ")>🔃</a>";
        var rate = "<select id=pbr" + i + " onchange=audioRate(" + i + ",'pbr" + i + "')><option value='0.5' >x0.5</option><option value='0.75'>x0.75</option><option value='1' selected>x1</option></select>";
        var top = "<a id=navButton href=#top>🔝</a>";
        var exP = "<a id=navButton href=#exercise" + (i - 1) + ">⬅️</a>";
        var exN = "<a id=navButton href=#exercise" + (i - -1) + ">➡️</a>";
        var line = "<hr style=height:1rem;border-radius:0.5rem;background-color:#75ab9a;border-style:none;>"
        text1 += img + "<div id=transport><div id=audioControl>" + aud + rate + "</div><div id=nav>" + top + exP + exN + "</div></div>" + "<br>" + line;
        text2 += "<a id=numberButton href=#exercise" + i + "> " + i + "</a>"
      }
       document.getElementById("music").innerHTML = text1;
       document.getElementById("numberSelect").innerHTML = text2;
     }
  </script>
  </body>