  <head>
  <style>
    img {
      height: auto;
      width: 100%;
      display: inline-block;
      margin-bottom: 0.5rem;
    }
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
      margin-bottom: 0.5rem;
      font-family: arial;
      font-size: 3rem;
      color: #75ab9a;
    }
    #exercises {
      display:flex;
      align-items: center;
      font-family: arial;
      font-size: 3rem;
    }
    #numberSelect {
      display: flex;
      flex-wrap: wrap;
      align-content: space-between;
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
  <div id="top" style="font-family:Arial, Helvetica, sans-serif">ESSENTIAL ELEMENTS FOR BAND:<br>BARITONE BOOK 1</div>
    <div id="exercises">
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
    //PLAY//
    function audioPlay(id) {
      var z = document.getElementById(id);
      z.play();
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
    const aud_dir = "https://e1-assets.s3.us-west-1.amazonaws.com/";
    const aud_name = "E1BB"
    const aud_path = `${aud_dir}${aud_name}`;
    const img_dir = "https://www.essentialelementsinteractive.com/EESONGS/Graphics/"
    const img_name = "B1BarBC";
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
        var img = "<img id=exercise" + i + " src=" + img_path + zero + i + ".jpg>";
        var play = "<a id=navButton onclick=audioPlay(" + i + ")>▶️</a>"
        var aud = "<audio id=" + i + " preload='none'><source src=" +  aud_path + i + ".mp3></audio><a id=navButton onclick=audioRestart(" + i + ")>🔃</a>";
        var rate = "<select id=pbr" + i + " onchange=audioRate(" + i + ",'pbr" + i + "')><option value='0.5' >x0.5</option><option value='0.75'>x0.75</option><option value='1' selected>x1</option></select>";
        var top = "<a id=navButton href=#top>🔝</a>";
        var exP = "<a id=navButton href=#exercise" + (i - 1) + ">⬅️</a>";
        var exN = "<a id=navButton href=#exercise" + (i - -1) + ">➡️</a>";
        var line = "<hr style=height:1rem;border-radius:0.5rem;background-color:#75ab9a;border-style:none;>"
        text1 += img + "<div id=transport><div id=audioControl>" + play + aud + rate + "</div><div id=nav>" + top + exP + exN + "</div></div>" + "<br>" + line;
        text2 += "<a id=numberButton href=#exercise" + i + "> " + i + "</a>"
      }
       document.getElementById("music").innerHTML = text1;
       document.getElementById("numberSelect").innerHTML = text2;
     }
  </script>
  </body>
