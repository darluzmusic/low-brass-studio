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
  <div id="top" style="font-family:Arial, Helvetica, sans-serif">ESSENTIAL ELEMENTS FOR JAZZ ENSEMBLE:<br>TROMBONE BOOK 1</div>
    <div id="exercises">
    <select id="exerciseSelect" onchange="selectFunction()">
    <option>1-5</option>
    <option>6-8</option>
    <option>9-13</option>
    <option>14-19</option>
    <option>20-24</option>
    <option>25-27</option>
    <option>28-30</option>
    <option>31-36</option>
    <option>37-41</option>
    <option>42-45</option>
    <option>46-50</option>
    <option>51-52</option>
    <option>53-57</option>
    <option>58-59</option>
    <option>60-65</option>
    <option>66-69</option>
    <option>70-75</option>
    <option>76-78</option>
    <option>79-80</option>
    <option>81-82</option>
    <option>83-86</option>
    <option>87-92</option>
    <option>93-98</option>
    <option>99-100</option>
    <option>101-107</option>
    <option>108-114</option>
    <option>115-118</option>
    <option>119-120</option>
    <option>121-121</option>
    <option>122-122</option>
  </select>
    <span class="navButton" onclick="pagePrevious(); selectFunction();">⬅️</span>
    <span class="navButton" onclick="pageNext(); selectFunction();">➡️</span>
    <span class="navButton" id="fs" onclick="fullScreen();">⛶</span>
    </div>
      <br>
  <div id="numberSelect"></div>
  <div id="music"></div>
  <hr style="height:1rem;
  border-radius:0.5rem;
  background-color:#75ab9a;
  border-style:none;">
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
    function audioPlay(id) {
      var z = document.getElementById(id);
      if (z.paused || z.ended) {
        z.play();
        document.getElementById("transport" + id).innerHTML = "⏸️";
      } else {
        z.pause();
        document.getElementById("transport" + id).innerHTML = "▶️";
      }
      }
    //RESTART//
    function audioRestart(id) {
      var y = document.getElementById(id);   
      y.currentTime=0;
      y.pause();
      document.getElementById("transport" + id).innerHTML = "▶️";
      }
    //PLAYBACKRATE//
    //Needed '' in function call to read as id//
    function audioRate(l,m) {
      var r = document.getElementById(l);
      var v = document.getElementById(m).value;
      r.playbackRate = v;
    }
    //LOOP//
    const dir = "https://low-brass-assets.s3.us-west-1.amazonaws.com/jz1/";

    function selectFunction() {
     let text1 = "";
     let text2 = "";
     var x = document.getElementById("exerciseSelect").value;
     const myArray = x.split("-");
     var h = myArray[0];
     var i = parseInt(h);
     var j = myArray[1];
     var num = parseInt(j);
     for (; i <= num; i++) 
      {
        //LOOP ELEMENTS//
        var img = "<img id=exercise" + i + " src=" + dir + i + ".jpg>";
        var play = "<span class=navButton id=transport" + i + " onclick=audioPlay(" + i + ")>▶️</span>"
        var aud = "<audio id=" + i + " preload='none'><source src=" + dir + i + ".mp3></audio><span class=navButton onclick=audioRestart(" + i + ")>🔃</span>";
        var rate = "<select id=pbr" + i + " onchange=audioRate(" + i + ",'pbr" + i + "')><option value='0.5' >x0.5</option><option value='0.75'>x0.75</option><option value='1' selected>x1</option></select>";
        var top = "<a class=navButton onclick=audioRestart(" + i + ") href=#top>🔝</a>";
        var exP = "<a class=navButton onclick=audioRestart(" + i + ") href=#line" + (i - 1) + ">⬅️</a>";
        var exN = "<a class=navButton onclick=audioRestart(" + i + ") href=#line" + (i - -1) + ">➡️</a>";
        var line = "<hr id=line" + i + " style=height:1rem;border-radius:0.5rem;background-color:#75ab9a;border-style:none;>"
        text1 += line + "<div id=transport><div id=audioControl>" + play + aud + rate + "</div><div id=nav>" + top + exP + exN + "</div></div>" + img;
        text2 += "<a class=numberButton href=#line" + i + "> " + i + "</a>"
      }
       document.getElementById("music").innerHTML = text1;
       document.getElementById("numberSelect").innerHTML = text2;
     }
  </script>
  </body>
