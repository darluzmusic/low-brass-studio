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
            <option value="1-1">1. The Green Danube</option>
            <option value="2-4">2. Tone Colors</option>
            <option value="3-7">3. Reaching Up</option>
            <option value="4-10">4. Uptown-Downtown</option>
            <option value="5-13">5. Main Street</option>
            <option value="6-16">6. Ski Slope</option>
            <option value="7-19">7. Doin’ Your Chords</option>
            <option value="8-22">8. Stop And Go</option>
            <option value="9-25">9. Glider</option>
            <option value="10-28">10. Jumper</option>
            <option value="11-31">11. Da Dit</option>
            <option value="12-34">12. Hot Fudge</option>
            <option value="13-37">13. Tijuana</option>
            <option value="14-40">14. La De Da De</option>
            <option value="15-43">15. Switcharoo</option>
            <option value="16-46">16. Swing Easy</option>
            <option value="17-49">17. Hop Scotch</option>
            <option value="18-52">18. Swingin’ In The Rain</option>
            <option value="19-55">19. 4/4 Waltz</option>
            <option value="20-58">20. One Note Break</option>
            <option value="21-61">21. Lazy</option>
            <option value="22-64">22. Bits And Pieces</option>
      </select>
      <a class="navButton" onclick="audioRestart(); pagePrevious(); selectFunction(); audioRate('track','pbr')">⬅️</a>
      <a class="navButton" onclick="audioRestart(); pageNext(); selectFunction(); audioRate('track','pbr')">➡️</a>
      <span class="navButton" id="fs" onclick="fullScreen();">⛶</span>
      <a id="transport" class="navButton" onclick="audioPlay();">▶️</a>
      <a class="navButton" onclick="audioRestart();">🔃</a>
      <select id="pbr" onchange="audioRate('track','pbr');">
        <option value="0.5" >x0.5</option>
        <option value="0.75">x0.75</option>
        <option value="1" selected>x1</option>
      </select>
      <select id="demoToggle" onchange="audioRestart(); selectFunction(); audioRate('track','pbr')">
        <option value="0">Complete</option>
        <option value="1">Minus 2nd</option>
        <option value="2">Minus 1st</option>
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
      z.onended = function() {
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
      const fol = "ejd/";
      const path = `${dir}${fol}`;
      function selectFunction() {
       let text1 = "";
       var l = document.getElementById("exerciseSelect").value;
       var n = document.getElementById("demoToggle").value;
       var demo = parseInt(n);
       const myArray = l.split("-");
       var h = myArray[0];
       var i = parseInt(h);
       var f = myArray[1];
       var k = parseInt(f);
       var text2 = path + (k + demo) + ".mp3";
          text1 += "<img id=tune" + i + " src=" + path + i + ".png>";
         document.getElementById("music").innerHTML = text1;
         document.getElementById("track").src = text2;
       }
  </script>
</body>