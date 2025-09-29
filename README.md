<h2>Calculadora de Juros</h2>
<label>Capital inicial (R$):</label>
<input type="number" id="capital"><br><br>

<label>Taxa de juros (%):</label>
<input type="number" id="taxa"><br><br>

<label>Tempo (meses):</label>
<input type="number" id="tempo"><br><br>

<button onclick="calcularJuros()">Calcular</button>

<p id="resultado"></p>

<script>
function calcularJuros() {
    let capital = parseFloat(document.getElementById("capital").value);
    let taxa = parseFloat(document.getElementById("taxa").value) / 100;
    let tempo = parseInt(document.getElementById("tempo").value);

    // Juros Compostos
    let montante = capital * Math.pow((1 + taxa), tempo);
    let juros = montante - capital;

    document.getElementById("resultado").innerHTML = 
        `Montante final: R$ ${montante.toFixed(2)} <br>
         Juros acumulados: R$ ${juros.toFixed(2)}`;
}
</script>
