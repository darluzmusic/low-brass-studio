<head>
<style>
.select {
    display: flex;
    justify-content: left;
}

.audio {
    display: flex;
    justify-content: center;
}

.music {
    display: flex;
    justify-content: center;
}
<style>
</head>
<body>
  <div class="select_audio">
  <p class="select"><select onchange="document.getElementById('music').src = this.value">
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd00.png">Sheet Music</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd01.png">Solo Guide</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd02.png">Roots</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd03.png">7ths to 3rds</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd04.png">1st 2 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd05.png">1st 3 Notes</option>
   <option value="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd06.png">Triads</option>
   </select></p>  
  <p class="audio"><audio controls>
    <source src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/audio/sd.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
   </audio><p>
  </div>
 <div class="sheet_music">
  <p class="music"<img id="music" src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/sd00.png"         width="100%"></p>
    </div>
</body>
