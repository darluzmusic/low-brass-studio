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
    <div id="exercises">
      <select id="exerciseSelect" onchange="selectFunction()">
        <option value="1-1-1">Long Tones</option>
        <option value="2-3-2">Tonguing</option>
        <option value="4-4-3">Fingers Wake-Up Call</option>
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
      <a id="navButton" onclick="pagePrevious(); selectFunction();">⬅️</a>
      <a id="navButton" onclick="pageNext(); selectFunction();">➡️</a>
      <a id="navButton" onclick="audioPlay();">▶️</a>
      <a id="navButton" onclick="audioRestart();">🔃</a>
      <select id="pbr" onchange="audioRate();">
        <option value="0.5" >x0.5</option>
        <option value="0.75">x0.75</option>
        <option value="1" selected>x1</option>
      </select>
      <select id="demoToggle" onchange="selectFunction();">
        <option value="0">w/ tuba</option>
        <option value="12">w/o tuba</option>
      </select>
      <audio id="track" preload="none"><source src=></audio>
    </div>
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
      function audioPlay() {
        var z = document.getElementById("track");
        z.play();
        }
      //RESTART//
      function audioRestart() {
        var y = document.getElementById("track");   
        y.currentTime=0;
        y.pause();
        }
      //PLAYBACKRATE//
      //Needed '' in function call to read as id//
      function audioRate() {
        var r = document.getElementById("track");
        var v = document.getElementById("pbr").value;
        r.playbackRate = v;
      }
      //LOOP//
      const dir = "https://low-brass-assets.s3.us-west-1.amazonaws.com/";
      const fol = "15mwu-tuba/";
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