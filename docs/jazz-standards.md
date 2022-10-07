---
layout: default
title: Jazz Standards
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
   <option value="https://darluzmusic.github.io/low-brass-studio/autumn-leaves">Autumn Leaves</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/days-of-wine-and-roses">Days of Wine and Roses</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/footprints">Footprints</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/just-friends">Just Friends</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/misty">Misty</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/satin-doll">Satin Doll</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/so-what">So What</option>
   <option value="https://darluzmusic.github.io/low-brass-studio/sesame-street">Sesame Street</option>
   </select>
</div>
<center>
<div class="sheet_music">
<iframe frameBorder="0" id="music" height="1920" src="https://darluzmusic.github.io/low-brass-studio/autumn-leaves" width="100%"></iframe>
</div>
<center>
<body>
