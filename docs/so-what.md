---
layout: default
title: So What
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
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw00.png">Sheet Music</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw01.svg">Scale | Whole</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw02.svg">3rds | Whole</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw03.svg">Broken Chords | Whole</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw04.svg">Scale | Half</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw05.svg">3rds | Half</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw06.svg">Broken Chords | Half</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw07.svg">Scale to 3rds</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw08.svg">Broken Chords to Scale</option>
   </select>
  <audio controls>
    <source src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/audio/sw.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
   </audio>
</div>
<center>
<div class="sheet_music">
<img id="music" src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sw00.png" width="100%">
</div>
<center>
<body>
