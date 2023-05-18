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
        <option value="1-1-1">Air It Out</option>
        <option value="2-2-2">Sound</option>
        <option value="3-4-3">Tonguing</option>
        <option value="5-6-4">Extended Slurs</option>
        <option value="7-7-5">Basic Flex</option>
        <option value="8-8-6">Flexing the 5th</option>
        <option value="9-9-7">Interval Flexibility</option>
        <option value="10-10-8">Broken Triads</option>
        <option value="11-12-9">Octaflex</option>
        <option value="13-13-10">Interval Attacks</option>
        <option value="14-14-11">5th Connection</option>
        <option value="15-15-12">Chromatic 4ths</option>
        <option value="16-17-13">Super 9ths</option>
        <option value="18-18-14">Control</option>
        <option value="19-19-15">Pedal Point</option>      
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
        <option value="15">w/o tuba</option>
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
      const fol = "20mwu-tuba/";
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
          var img = "<img src=" + path + i + ".jpg>";
          text1 += img ;
        }
         document.getElementById("music").innerHTML = text1;
         document.getElementById("track").src = text2;
       }
  </script>
</body>