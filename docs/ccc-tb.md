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
        <option value="1-1-1">1. “Après un Rêve (After A Dream), Op. 7, No. 1” by Gabriel Fauré</option>
        <option value="2-2-2">2. “Valse Sentimentale” by P. I. Tschaikowsky</option>
        <option value="3-3-3">3. “Canzonetta” by W. A. Mozart</option>
        <option value="4-5-4">4. “Two Spanish Dances” by Leroy Ostransky</option>
        <option value="6-6-5">5. “Thème de Concours” by Robert Clérisse</option>
        <option value="7-7-6">6. “Sarabande and Vivace” by G. F. Handel</option>
        <option value="8-9-7">7. “Love Thoughts” by Arthur Pryor</option>
        <option value="10-11-8">8. “Morceau de Concours” by Edmond Missa</option>
        <option value="12-13-9">9. “Crépuscule” by Gabriel Parès</option>
        <option value="14-15-10">10. “Concerto Miniature” by Leroy Ostransky</option>
        <option value="16-17-11">11. “Prelude and Fanfaronade” by Paul Koepke</option>
        <option value="18-19-12">12. “Solo de Concert” by Th. Dubois</option>
        <option value="20-21-13">13. “Concerto in F Minor” by Émile Lauga</option>
        <option value="22-22-14">14. “Allegro Vivace from Concerto” by N. Rimsky-Korsakoff</option>
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
        <option value="0">w/ trb</option>
        <option value="14">w/o trb</option>
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
      const fol = "ccc-tb/";
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
          var img = "<img id=tune" + i + " src=" + path + i + ".png>";
          text1 += "<a href=#tune" + (i - -1) + ">" + img + "</a>";
        }
         document.getElementById("music").innerHTML = text1;
         document.getElementById("track").src = text2;
       }
  </script>
</body>