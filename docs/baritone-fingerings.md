<!DOCTYPE html>
<html>
<head>
<style>
body { font-family: sans-serif; 
       background-color: #92a8d1;
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
  transition: transform 1s;
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
<div class="scene scene--card">
  <div class="card">
    <div class="card__face card__face--front"><img src="https://github.com/darluzmusic/low-brass-studio/raw/master/docs/assets/fc01.png" alt="sheet music" width="90%" ></div>
    <div class="card__face card__face--back"><p>E<p><p>⚫⚫⚫<p><p>1 2 3<p></div>
  </div>
</div>
<center>
<script>
var card = document.querySelector('.card');
card.addEventListener( 'click', function() {
  card.classList.toggle('is-flipped');
});
</script>
</body>
</html>

