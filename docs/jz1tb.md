<body>
    <h1>ESSENTIAL ELEMENTS FOR JAZZ ENSEMBLE:</h1>
      <h2>TROMBONE BOOK 1</h2>
      Exercises: 
      <select id="exerciseSelect" onchange="selectFunction()">
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_01.png">1-5</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_02.png">6-8</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_03.png">9-13</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_04.png">14-19</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_05.png">20-24</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_06.png">25-27</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_07.png">28-30</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_08.png">31-36</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_09.png">37-41</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_10.png">42-45</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_11.png">46-50</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_12.png">51-52</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_13.png">53-57</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_14.png">58-59</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_15.png">60-65</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_16.png">66-69</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_17.png">70-75</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_18.png">76-78</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_19.png">79-80</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_20.png">81-82</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_21.png">83-86</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_22.png">87-92</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_23.png">93-98</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_24.png">99-100</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_25.png">101-107</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_26.png">108-114</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_27.png">115-118</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_28.png">119-120</option>
        <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_29.png">121</option>
    </select>
    <button onclick="exercise_previous(); selectFunction(); playFunction();">⬅️</button>
    <button onclick="exercise_next(); selectFunction(); playFunction();">➡️</button>
    <br>
    Play-along:
    <select id="playSelect" onchange="playFunction()">
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll1.mp3">1. ATTACKS AND RELEASES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll2.mp3">2. ACCENTING 2 AND 4</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll3.mp3">3. DOO AND BAH</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll4.mp3">4. DIT AND DOT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll5.mp3">5. DOO, BAH, DIT, AND DOT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll6.mp3">6. SWING 8TH NOTES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll7.mp3">7. QUARTERS AND 8THS</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll8.mp3">8. MORE QUARTERS AND 8THS</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll9.mp3">9. SWINGIN' THE SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll10.mp3">10. MOVIN' AROUND</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll11.mp3">11. RUNNIN' AROUND</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll12.mp3">12. TRADIN' OFF</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll13.mp3">13. JA-DA</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll14.mp3">14. SYNCOPATING BY ANTICIPATING THE BEAT (PLAYING EARLY)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll15.mp3">15. SYNCOPATING BY DELAYING THE BEAT (PLAYING LATE)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll16.mp3">16. WHEN THE SAINTS GO MARCHING IN - Without Syncopation</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll17.mp3">17. WHEN THE SAINTS GO MARCHING IN -With Syncopation</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll18.mp3">18. RHYTHM STUDY FOR JA-DA</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll19.mp3">19. JA-DA - Full Band Arrangement - With Syncopation</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll20.mp3">20. READING SWING RHYTHMS</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll21.mp3">21. SWING RHYTHM WORKOUT #1</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll22.mp3">22. SWING RHYTHM WORKOUT #2</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll23.mp3">23. SWING RHYTHM WORKOUT #3</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll24.mp3">24. SWING RHYTHM REVIEW</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll25.mp3">25. JAZZIN' UP A-TISKET A-TASKET</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll26.mp3">26. JAZZIN' UP JINGLE BELLS</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll27.mp3">27. LONDON BRIDGE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll28.mp3">28. RHYTHM WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll29.mp3">29. MELODY WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll30.mp3">30. SWINGIN' WITH JACK - Full Band Arrangement</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll31.mp3">31. MAJOR SEVENTH SCALE AND CHORD</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll32.mp3">32. DOMINANT AND MINOR SEVENTH CHORD</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll33.mp3">33. MAJOR SEVENTH CHORD WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll34.mp3">34. DOMINANT SEVENTH CHORD WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll35.mp3">35. MINOR SEVENTH CHORD WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll36.mp3">36. LISTEN TO THE BLUES PROGRESSION - Bb Concert</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll37.mp3">37. BLUES WORKOUT - Roots and Sevenths</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll38.mp3">38. BLUES WORKOUT - Roots, Thirds, and Sevenths</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll39.mp3">39. MAKE UP YOUR OWN - 2-Bar Solos using Roots, Thirds, and Sevenths</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll40.mp3">40. BLUES WORKOUT - Dominant Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll41.mp3">41. BLUES WORKOUT - Scale steps 1, 2, and 3</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll42.mp3">42. BLUES WORKOUT - Scale steps 1 through 5</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll43.mp3">43. BLUES WORKOUT - Scale steps 1 through 5, and b7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll44.mp3">44. MAKE UP YOUR OWN - 2-Bar Solos</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll45.mp3">45. OUR FIRST BLUES - Full Band Arrangement with Solos</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll46.mp3">46. RHYTHM WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll47.mp3">47. MELODY WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll48.mp3">48. LISTEN TO THE CHORDS FOR ST. LOUIS BLUES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll49.mp3">49. BLUES WORKOUT FOR ST. LOUIS BLUES - Roots, Thirds, and Sevenths</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll50.mp3">50. BLUES WORKOUT FOR ST. LOUIS BLUES - Scale steps 1 through 5, and b7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll51.mp3">51. "JAZZIN', UP" ST. LOUIS BLUES - Adding Rhythms</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll52.mp3">52. ST. LOUIS BLUES - Add Your Own Rhythms</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll53.mp3">53. ST. LOUIS BLUES - Original Melody</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll54.mp3">54. ST. LOUIS BLUES - Changing Rhythms</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll55.mp3">55. ST. LOUIS BLUES - Repeating Parts of the Melody</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll56.mp3">56. ST. LOUIS BLUES - Filling in the Skips</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll57.mp3">57. ST. LOUIS BLUES - Adding "Wrong" Notes (Chromatic Ornamentation)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll58.mp3">58. ST. LOUIS BLUES - Full Band Arrangement</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll59.mp3">59. DEMONSTRATION SOLO FOR ST. LOUIS BLUES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll60.mp3">60. BLUES SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll61.mp3">61. THE BLUES SCALE - With the Blues Progression</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll62.mp3">62. BLUES WORKOUT - Blues Scale ( 1, b3, and 4)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll63.mp3">63. BLUES WORKOUT - Blues Scale ( 1, b3, 4, and b5)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll64.mp3">64. BLUES WORKOUT - Blues Scale ( 1, b3, 4, b5, 5, and b7)</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll65.mp3">65. MAKE UP YOUR OWN - 2-Bar Solos</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll66.mp3">66. RHYTHM WORKOUT #1</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll67.mp3">67. RHYTHM WORKOUT #2</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll68.mp3">68. COMMON RIFFS - Using Notes of the Blues Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll69.mp3">69. MORE COMMON RIFFS - Using Notes of the Blues Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll70.mp3">70. THE MAJOR BLUES SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll71.mp3">71. COMPARE THE BLUES SCALES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll72.mp3">72. THE BEND</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll73.mp3">73. THE SCOOP</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll74.mp3">74. MAKING THE BLUES SCALES SOUND "BLUESY"</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll75.mp3">75. COMMON RIFFS - Using Notes of the Major Blues Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll76.mp3">76. MORE COMMON RIFFS - Using Notes of the Blues Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll77.mp3">77. QUESTIONS AND ANSWERS</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll78.mp3">78. TRADING OFF - Questions and Answers</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll79.mp3">79. MAKE UP YOUR OWN ANSWER WITH THE BLUES SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll80.mp3">80. MAKE UP YOUR OWN QUESTION WITH THE MAJOR BLUES SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll81.mp3">81. "RIFFIN' AROUND" - Full Band Arrangement</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll82.mp3">82. DEMONSTRATION SOLO FOR "RIFFIN' AROUND"</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll83.mp3">83. RHYTHM WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll84.mp3">84. MELODY WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll85.mp3">85. MIXOLYDIAN WORKOUT - Scale Steps 1-5</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll86.mp3">86. MIXOLYDIAN WORKOUT - Scale Steps 1-7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll87.mp3">87. WRONG NOTES CAN SOUND WRONG</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll88.mp3">88. WRONG NOTES CAN SOUND GOOD</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll89.mp3">89. CHROMATIC WORKOUT - Filling in the Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll90.mp3">90. CHROMATIC WORKOUT - Filling in the Scale with Triplets</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll91.mp3">91. CHROMATIC WORKOUT - Enclosing the Good Notes</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll92.mp3">92. CHROMATIC WORKOUT - Using the Bebop Lick</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll93.mp3">93. COMPARE THE MIXOLYDIAN MODE AND THE BEBOP SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll94.mp3">94. BEBOP SCALE WORKOUT - Running Down the Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll95.mp3">95. BEBOP SCALE WORKOUT - Running Down from 3 to 7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll96.mp3">96. BEBOP SCALE WORKOUT - Running Up from 5 and Ending on 7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll97.mp3">97. BEBOP SCALE WORKOUT - Keeping the 8th Notes Going</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll98.mp3">98. TRADING OFF WITH THE BEBOP SCALE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll99.mp3">99. "BOPPIN' AROUND" - Full Band Arrangement</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll100.mp3">100. DEMONSTRATION SOLO FOR "BOPPIN' AROUND"</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll101.mp3">101. COMPARE THE 8TH NOTES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll102.mp3">102. QUARTER NOTES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll103.mp3">103. 8TH NOTES</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll104.mp3">104. LATIN/ROCK RHYTHM WORKOUT #1</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll105.mp3">105. LATIN/ROCK RHYTHM WORKOUT #2</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll106.mp3">106. LATIN/ROCK RHYTHM WORKOUT #3</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll107.mp3">107. MAKE UP YOUR OWN</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll108.mp3">108. RHYTHM WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll109.mp3">109. MELODY WORKOUT</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll110.mp3">110. MINOR SEVENTH CHORD</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll111.mp3">111. DORIAN MODE WORKOUT - Scale Steps 1-5</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll112.mp3">112. DORIAN MODE WORKOUT - Scale Steps 1-8</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll113.mp3">113. DORIAN MODE WORKOUT - Scale Steps 1-9</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll114.mp3">114. DORIAN MODE WORKOUT - Skipping notes and moving around</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll115.mp3">115. MAKE UP YOUR OWN - 2-Bar Solos Using the Dorian Mode</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll116.mp3">116. BLUES SCALE WORKOUT - 1, b3, 4, 5, and b5</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll117.mp3">117. BLUES SCALE WORKOUT - 1, b3, 4, b5, and b7</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll118.mp3">118. MAKE UP YOUR OWN - 2-Bar Solos Using the Blues Scale</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll119.mp3">119. SALSA CALIENTE - Full Band Arrangement</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll120.mp3">120. DEMONSTRATION SOLO FOR SALSA CALIENTE</option>
      <option value="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll121.mp3">121. Jazz Ornamentation and Expression</option>
      </select>   
      <button onclick="play_previous(); playFunction();">⬅️</button>
      <button onclick="play_next(); playFunction();">➡️</button>
      <br>
      <audio id="play" controls>
        <source src="https://jz1-assets.s3.us-west-1.amazonaws.com/JzAll1.mp3">
      </audio>
      <br>
      <img id="exercise" width="100%" src="https://jz1-assets.s3.us-west-1.amazonaws.com/jz1_Page_01.png">
      
    <script>
    //PLAYALONG//
    function playFunction() {
        var z =
    document.getElementById("playSelect").value;
        var a =
    document.getElementById("play");
    a.src = z;
    }

    //BUTTONS//
    function exercise_previous() {
        var x = 
    document.getElementById("exerciseSelect").selectedIndex;
    document.getElementById("exerciseSelect").selectedIndex = x - 1;
    }
    function exercise_next() {
        var x = 
    document.getElementById("exerciseSelect").selectedIndex;
    document.getElementById("exerciseSelect").selectedIndex = x + 1;
    }
    function play_previous() {
        var y = 
    document.getElementById("playSelect").selectedIndex;
    document.getElementById("playSelect").selectedIndex = y - 1;
    }
    function play_next() {
        var y = 
    document.getElementById("playSelect").selectedIndex;
    document.getElementById("playSelect").selectedIndex = y + 1;
    }

    //EXERCISES//
    function selectFunction() {
      var x = document.getElementById("exerciseSelect").value;
      document.getElementById("exercise").src = x;
      var u = document.getElementById("exerciseSelect").selectedIndex;
      var v = document.getElementById("exerciseSelect").options;
      var w = v[u].text;

      const myArray = w.split("-");
      document.getElementById("playSelect").selectedIndex = myArray[0] - 1;
    }
    </script>
    </body>
