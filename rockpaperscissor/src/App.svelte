<script>
  let resultEl,
    computerScore = 0,
    playerScore = 0,
    totolRounds = 0;
  function handleEvent(move) {
    totolRounds++;
    playRound(move.currentTarget.id, computerPlay());
  }

  function computerPlay() {
    const choices = ["rock", "paper", "scissor"];
    const choice = Math.floor(Math.random() * choices.length);
    return choices[choice];
  }
  function playRound(p, c) {
    if (c == p) {
      resultEl = "It's a tie";
    } else if (
      (c == "rock" && p == "scissor") ||
      (c == "scissor" && p == "paper") ||
      (c == "paper" && p == "rock")
    ) {
      resultEl = "Computer Wins 🤖";
      computerScore++;
    } else {
      resultEl = "You Wins 🧑";
      playerScore++;
    }
  }
</script>

<div class="container">
  <div class="content">
    <h1>Rock Papper Scissor</h1>
    <div class="game">
      <h3>Choose your move</h3>
      <div class="moves">
        <button class="move" id="rock" onclick={handleEvent}> 👊 </button>
        <button class="move" id="paper" onclick={handleEvent}> 🖐️ </button>
        <button class="move" id="scissor" onclick={handleEvent}> ✌️ </button>
      </div>
      <div class="result" id="result">{resultEl}</div>
      <div class="info">
        <span class="scores">
          your score :<span class="player" id="player">{playerScore}</span>
          Computer score : <span class="bot" id="bot">{computerScore}</span>
        </span>
        <span class="total" id="total"> Total games : {totolRounds}</span>
      </div>
    </div>
  </div>
</div>
