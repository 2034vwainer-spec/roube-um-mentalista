<style>
#mentalista-boss {
  position: fixed;
  top: 15px;
  right: 15px;
  width: 250px;
  padding: 15px;
  color: white;
  background: #180b2e;
  border: 2px solid #a855f7;
  border-radius: 15px;
  font-family: Arial, sans-serif;
  z-index: 99999;
  box-shadow: 0 0 20px #a855f7;
}
#mentalista-boss button {
  padding: 10px;
  border: 0;
  border-radius: 8px;
  background: #a855f7;
  color: white;
  font-weight: bold;
  cursor: pointer;
}
#boss-vida {
  height: 15px;
  background: #ef4444;
  width: 100%;
  border-radius: 10px;
  transition: width .2s;
}
#boss-barra {
  background: #444;
  border-radius: 10px;
  overflow: hidden;
  margin: 10px 0;
}
</style>

<div id="mentalista-boss">
  <h3>👑 MENTALISTA SUPREMO</h3>
  <div>❤️ Vida: <span id="boss-hp">5000</span> / 5000</div>
  <div id="boss-barra">
    <div id="boss-vida"></div>
  </div>
  <p id="boss-status">O chefe está esperando um desafio!</p>
  <button onclick="atacarMentalista()">⚔️ ATACAR BOSS</button>
</div>

<script>
(function () {
  let vida = 5000;
  let derrotado = false;

  window.atacarMentalista = function () {
    if (derrotado) return;

    vida = Math.max(0, vida - 250);

    document.getElementById("boss-hp").textContent = vida;
    document.getElementById("boss-vida").style.width =
      (vida / 5000 * 100) + "%";

    const status = document.getElementById("boss-status");

    if (vida === 0) {
      derrotado = true;
      status.textContent = "🏆 BOSS DERROTADO! Você venceu!";
      document.querySelector("#mentalista-boss button").disabled = true;
    } else {
      status.textContent =
        vida <= 2500
          ? "😈 O boss está furioso! Vida restante: " + vida
          : "⚡ Você acertou! O boss perdeu 250 de vida!";
    }
  };
})();
</script>
