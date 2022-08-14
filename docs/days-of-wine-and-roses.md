---
layout: default
title: Days of Wine & Roses
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
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr00.svg">Sheet Music</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr01.svg">Solo Guide</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr02.svg">Roots</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr03.svg">7ths to 3rds</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr04.svg">1st 2 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr05.svg">1st 3 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr06.svg">Triads</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr07.svg">1st 5 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr08.svg">7th Chords</option>
   </select>
  <audio id="myAudio" controls>
    <source src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/audio/wr.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
   </audio>
     <div class="pbr_form">
      <form>
       <span id="currentPbr">1</span>
       <input id="pbr" type="range" value="1" 
                    min="0.25" max="2" step="0.25" >
 
     </form>
    </div>
</div>
<center>
<div class="sheet_music">
<img id="music" src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/wr00.svg" width="100%">
</div>
<center>
<body>
