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
<option value="1-1-1"> No. 1</option>
<option value="2-2-2"> No. 2</option>
<option value="3-3-3"> No. 3</option>
<option value="4-4-4"> No. 4</option>
<option value="5-5-5"> No. 5</option>
<option value="6-6-6"> No. 6</option>
<option value="7-7-7"> No. 7</option>
<option value="8-8-8"> No. 8</option>
<option value="9-10-9"> No. 9</option>
<option value="11-12-10"> No. 10</option>
<option value="13-14-11"> No. 11</option>
<option value="15-15-12"> No. 12</option>
<option value="16-16-13"> No. 13</option>
<option value="17-17-14"> No. 14</option>
<option value="18-19-15"> No. 15</option>
<option value="20-21-16"> No. 16</option>
<option value="22-23-17"> No. 17</option>
<option value="24-25-18"> No. 18</option>
<option value="26-27-19"> No. 19</option>
<option value="28-29-20"> No. 20</option>
<option value="30-31-21"> No. 21</option>
<option value="32-33-22"> No. 22</option>
<option value="34-34-23"> No. 23</option>
<option value="35-35-24"> No. 24</option>
<option value="36-37-25"> No. 25</option>
<option value="38-39-26"> No. 26</option>
<option value="40-40-27"> No. 27</option>
<option value="41-42-28"> No. 28</option>
<option value="43-44-29"> No. 29</option>
<option value="45-46-30"> No. 30</option>
<option value="47-47-31"> No. 31</option>
<option value="48-48-32"> No. 32</option>
<option value="49-50-33"> No. 33</option>
<option value="51-52-34"> No. 34</option>
<option value="53-53-35"> No. 35</option>
<option value="54-55-36"> No. 36</option>
<option value="56-57-37"> No. 37</option>
<option value="58-58-38"> No. 38</option>
<option value="59-60-39"> No. 39</option>
<option value="61-62-40"> No. 40</option>
<option value="63-64-41"> No. 41</option>
<option value="65-66-42"> No. 42</option>
<option value="67-68-43"> No. 43</option>
<option value="69-69-44"> No. 44</option>
<option value="70-71-45"> No. 45</option>
<option value="72-73-46"> No. 46</option>
<option value="74-75-47"> No. 47</option>
<option value="76-77-48"> No. 48</option>
<option value="78-79-49"> No. 49</option>
<option value="80-81-50"> No. 50</option>
<option value="82-83-51"> No. 51</option>
<option value="84-85-52"> No. 52</option>
<option value="86-86-53"> No. 53</option>
<option value="87-87-54"> No. 54</option>
<option value="88-89-55"> No. 55</option>
<option value="90-91-56"> No. 56</option>
<option value="92-93-57"> No. 57</option>
<option value="94-95-58"> No. 58</option>
<option value="96-97-59"> No. 59</option>
<option value="98-99-60"> No. 60</option>    
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
      const fol = "bordogni-tuba/";
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