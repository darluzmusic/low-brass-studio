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
        <option value="1-1-1">1. Sarabanda and Gavotta (Corelli)</option>
        <option value="2-2-2">2. Dedication (Zueignung) (R. Strauss)</option>
        <option value="3-3-3">3. Premier Solo de Concours (Maniet)</option>
        <option value="4-4-4">4. Calm As the Night (Böhm)</option>
        <option value="5-5-5">5. Andante and Allegro (Clérisse)</option>
        <option value="6-6-6">6. Romance in E♭ (Ostransky)</option>
        <option value="7-8-7">7. Air Gai (Berlioz)</option>
        <option value="9-10-8">8. Orientale (Barat)</option>
        <option value="11-11-9">9. Élégie (Duquesne)</option>
        <option value="12-12-10">10. Serenade, Op. 22, No. 1 (Böhm)</option>
        <option value="13-14-11">11. My Regards (Llewellyn)</option>
        <option value="15-16-12">12. L’Allegro (The Merry Man) (Koepke)</option>
        <option value="17-18-13">13. Petite Pièce Concertante (Balay)</option>
        <option value="19-20-14">14. Morceau de Concours, Op. 57 (Alary)</option>
        <option value="21-22-15">15. Concertino (Ostransky)</option>
        <option value="23-23-16">16. Andante (from Concerto in E♭) (Haydn)</option>
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
        <option value="0">Perf</option>
        <option value="16">Acc</option>
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
      const fol = "ccc-barbc/";
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