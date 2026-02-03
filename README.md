# Manav-sumayya1
function yesClicked() {
  document.getElementById("music").play();

  document.body.innerHTML = `
    <h1>Manav ❤️ Sumayya</h1>

    <img src="couple.jpg" 
         style="
           width:260px;
           height:260px;
           border-radius:20px;
           object-fit:cover;
           border:5px solid white;
           box-shadow:0 0 20px rgba(0,0,0,0.4);
           margin:20px 0;
         ">

    <h1>Forever & Always 💕</h1>
  `;

  const end = Date.now() + 6000;
  (function frame() {
    confetti({
      particleCount: 6,
      spread: 80,
      emojis: ["❤️","💖","💕","💘"],
      emojiSize: 28
    });
    if (Date.now() < end) requestAnimationFrame(frame);
  })();
}
