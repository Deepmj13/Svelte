<script>
  const moves = document.querySelectorAll("#move");
</script>

<div class="container">
  <div class="content">
    <h1>Rock Papper Scissor</h1>
    <div class="game">
      <h3>Choose your move</h3>
      <div class="moves">
        <span class="move" id="move"> 👊 </span>
        <span class="move" id="move"> 🖐️ </span>
        <span class="move" id="move"> ✌️ </span>
      </div>
      <div class="result" id="result"></div>
      <div class="info">
        <span class="scores">
          <span class="player" id="player"> your score : </span>
          <span class="bot" id="bot"> your score : </span>
        </span>
        <span class="total" id="total"> Total games : </span>
      </div>
    </div>
  </div>
</div>
