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
      flex-wrap: wrap;
      font-family: arial;
      font-size: 3rem;
    }
    .numberButton {
      font-family:Arial, Helvetica, sans-serif;
      font-size: 2rem;
      border-radius: 0.5rem;
      background-color: #75ab9a;
      color: white;
      padding: 1rem;
      margin: 0.1rem;
      text-decoration: none;
    }
    .numberButton:hover {
      text-decoration:none;
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
    .navButton {
      cursor: pointer;
      font-size: 2rem;
      border-radius: 0.5rem;
      background-color: #75ab9a;
      color: white;
      padding: 1rem;
      margin: 0.1rem;
      text-decoration: none;
    }
    .navButton:hover {
      text-decoration:none;
    }
    #pad {
      height: 1440px;
    }
  </style>
</head>
<body onload="selectFunction()" style="background-color:white">
    <div id="exercises">
      <select id="exerciseSelect" style="width: 18rem;" onchange="selectFunction(); audioRestart(); audioRate('track','pbr')">
        <option value="1-1-1">Long Tones</option>
        <option value="2-3-2">Tonguing</option>
        <option value="4-4-3">Embouchure Wake-Up Call</option>
        <option value="5-5-4">Lip Slurs</option>
        <option value="6-6-5">Flexibility</option>
        <option value="7-7-6">Triad Flexibility</option>
        <option value="8-8-7">Arpeggiated Flexibility</option>
        <option value="9-10-8">Open 5ths</option>
        <option value="11-11-9">Chromatic Flexibility</option>
        <option value="12-13-10">Major Scales</option>
        <option value="14-14-11">Upper Range</option>
        <option value="15-15-12">Warm Down</option>        
      </select>
      <a class="navButton" onclick="audioRestart(); pagePrevious(); selectFunction(); audioRate('track','pbr')">⬅️</a>
      <a class="navButton" onclick="audioRestart(); pageNext(); selectFunction(); audioRate('track','pbr')">➡️</a>
      <span class="navButton" id="fs" onclick="fullScreen();">⛶</span>
      <a id="transport" class="navButton" onclick="audioPlay();">▶️</a>
      <a class="navButton" onclick="audioRestart();">🔃</a>
      <select id="pbr" onchange="audioRate('track','pbr');">
        <option value="0.5" >x0.5</option>
        <option value="0.625" >x0.625</option>
        <option value="0.75">x0.75</option>
        <option value="0.875">x0.875</option>
        <option value="1" selected>x1</option>
        <option value="2">x2</option>
      </select>
      <select id="demoToggle" onchange="audioRestart(); selectFunction(); audioRate('track','pbr')">
        <option value="0">w/ trb</option>
        <option value="12">w/o trb</option>
      </select>
      <audio id="track" preload="none"><source src=></audio>
    </div>
    <div id="music"></div>
    <div id="pad"></div>
  <script>
    //FULLSCREEN//
    var elem = document.documentElement;  
    function fullScreen () {
    if (!document.fullscreenElement) {
      if (elem.requestFullscreen) {
      elem.requestFullscreen();
      } else if (elem.webkitRequestFullscreen) { /* Safari */
      elem.webkitRequestFullscreen();
      } else if (elem.msRequestFullscreen) { /* IE11 */
      elem.msRequestFullscreen();
      }
      return;
      }
      if (document.exitFullscreen) {
      document.exitFullscreen();
      } else if (document.webkitExitFullscreen) { /* Safari */
      document.webkitExitFullscreen();
      } else if (document.msExitFullscreen) { /* IE11 */
      document.msExitFullscreen();
      }
      }
    //BUTTONS//
    function pagePrevious() {
      var x = 
      document.getElementById("exerciseSelect").selectedIndex;
      if (x > 0) {
        document.getElementById("exerciseSelect").selectedIndex = x - 1;
      }
      }
    function pageNext() {
      var x = 
      document.getElementById("exerciseSelect").selectedIndex;
      var s = 
      document.getElementById("exerciseSelect").length;
      if (x < s - 1) {
        document.getElementById("exerciseSelect").selectedIndex = x + 1;
      }
      }
    //PLAY//
    function audioPlay() {
      var z = document.getElementById("track");
      if (z.paused || z.ended) {
        z.play();
        document.getElementById("transport").innerHTML = "⏸️";
      } else {
        z.pause();
        document.getElementById("transport").innerHTML = "▶️";
      }
      }
    //RESTART//
    function audioRestart() {
      var y = document.getElementById("track");   
      y.currentTime=0;
      y.pause();
      document.getElementById("transport").innerHTML = "▶️";
      }
    //PLAYBACKRATE//
    //Needed '' in function call to read as id//
    function audioRate(l,m) {
      var r = document.getElementById(l);
      var v = document.getElementById(m).value;
      r.playbackRate = v;
    }
    //LOOP//
      const dir = "https://low-brass-assets.s3.us-west-1.amazonaws.com/";
      const fol = "15mwu-trombone/";
      const path = `${dir}${fol}`;
      function selectFunction() {
       let text1 = "";
       var l = document.getElementById("exerciseSelect").value;
       var n = document.getElementById("demoToggle").value;
       var demo = parseInt(n);
       const myArray = l.split("-");
       var h = myArray[0];
       var i = parseInt(h);
       var j = myArray[1];
       var num = parseInt(j);
       var f = myArray[2];
       var k = parseInt(f);
       var text2 = path + (k + demo) + ".mp3";
       for (; i <= num; i++) 
          {
          var img = "<img src=" + path + i + ".png>";
          text1 += img ;
        }
         document.getElementById("music").innerHTML = text1;
         document.getElementById("track").src = text2;
       }
  </script>
</body>