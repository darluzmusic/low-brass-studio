<head>
<style>
body { font-family: sans-serif; 
       background-image: linear-gradient(120deg, #155799, #159957);
}

.scene {
  width: 360px;
  height: 240px;
  margin: 40px 0;
  perspective: 600px;
}

.card {
  position: relative;
  width: 100%;
  height: 100%;
  cursor: pointer;
  transform-style: preserve-3d;
  transform-origin: center right;
  transition: transform 0.5s;
}

.card.is-flipped {
  transform: translateX(-100%) rotateY(-180deg);
}

.card__face {
  position: absolute;
  width: 100%;
  height: 100%;
  line-height: 20px;
  color: black;
  text-align: center;
  font-weight: bold;
  font-size: 40px;
  backface-visibility: hidden;
}

.card__face--front {
  display:flex;
  justify-content:center;
  align-items:center;
  background: white;
}

.card__face--back {
  display:flex;
  justify-content:center;
  align-items:center;
  background: white;
  transform: rotateY(180deg);
}

</style>
</head>
<body>
<center>
<h1>Look at the front of each flashcard and say the note name and slide position out loud. For the first flashcard, you would say, "A-flat, 3rd position." Then, click on the flashcard to see the answer. If you don't know the answer, you can click on the flashcard first.<h1>       

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc05.1.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct05a.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc06.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct06.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc07.1.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct07a.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc09.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct09.png" alt="sheet music" width="90%"></div>
  </div>
</div>
       
<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc10.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct10.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc11.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct11.png" alt="sheet music" width="90%"></div>
  </div>
</div>     

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc12.1.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct12a.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc13.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct13.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc14.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct14.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc15.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct15.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc16.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct16.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc17.1.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct17a.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc18.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct18.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc19.1.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct19a.png" alt="sheet music" width="90%"></div>
  </div>
</div>

<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc21.png" alt="sheet music" width="90%"></div>
    <div class="card__face card__face--back"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fct21.png" alt="sheet music" width="90%"></div>
  </div>
</div>
       
<script>
var cards = document.querySelectorAll('.card');

[...cards].forEach((card)=>{
  card.addEventListener( 'click', function() {
    card.classList.toggle('is-flipped');
  });
});
</script>
<center>

