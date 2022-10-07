---
layout: default
title: Footprints
---
<head>
<script>
window.onload = function () {
 
  var v = document.getElementById("myAudio");
  var p = document.getElementById("pbr");
  var c = document.getElementById("currentPbr");
 
  p.addEventListener('input',function(){
    c.innerHTML = p.value;
    v.playbackRate = p.value;
  },false);
 
};
</script>
<style>
.audio_select {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding-top: 6px;
  padding-bottom: 6px;
  border: 2px black;
  border-style: hidden
}
.sheet_music {
  border: 2px black;
  border-style: hidden
}
.pbr_form {
  text-align: center;
  padding-left: 6px;
  padding-right: 6px;
  border: 2px black;
  border-style: hidden
}
</style>
</head>
<body>
<div class="audio_select">
  <select onchange="document.getElementById('music').src = this.value">
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fp00.jpg">Sheet Music</option>
   </select>
  <audio id="myAudio" controls>
    <source src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/audio/fp.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
   </audio>
   <div class="pbr_form">
      <form>
       <span id="currentPbr">1</span><br>
       <input id="pbr" type="range" value="1" 
                    min="0.25" max="2" step="0.25" >
 
     </form>
    </div>
</div>
<center>
<div class="sheet_music">
<img id="music" src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fp00.jpg" width="100%">
</div>
<center>
<body>
