---
layout: default
title: Just Friends
---
<head>
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
</style>
</head>
<body>
<div class="audio_select">
  <select onchange="document.getElementById('music').src = this.value">
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf00.png">Sheet Music</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf01.svg">Solo Guide</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf02.svg">Roots</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf03.svg">7ths to 3rds</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf04.svg">1st 2 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf05.svg">1st 3 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf06.svg">Triads</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf07.svg">1st 5 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf08.svg">7th Chords</option>
   </select>
  <audio controls>
    <source src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/audio/jf.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
   </audio>
</div>
<center>
<div class="sheet_music">
<img id="music" src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/jf00.png" width="100%">
</div>
<center>
<body>
