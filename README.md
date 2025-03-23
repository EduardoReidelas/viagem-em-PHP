<?php
function obterEntrada($prompt) {
    echo $prompt;
    return trim(fgets(STDIN));
}


$distancia = obterEntrada("Digite a distância da viagem (em km): ");
$consumo = obterEntrada("Digite o consumo do carro (km por litro): ");
$precoCombustivel = obterEntrada("Digite o preço do combustível (R$ por litro): ");

$distancia = (float)$distancia;
$consumo = (float)$consumo;
$precoCombustivel = (float)$precoCombustivel;

$litrosNecessarios = $distancia / $consumo;

$custoTotal = $litrosNecessarios * $precoCombustivel;

// Exibe os resultados
echo "\nResultado do Cálculo:\n";
echo "Distância da viagem: " . $distancia . " km\n";
echo "Consumo do carro: " . $consumo . " km/l\n";
echo "Preço do combustível: R$ " . number_format($precoCombustivel, 2, ',', '.') . " por litro\n";
echo "Litros necessários para a viagem: " . number_format($litrosNecessarios, 2, ',', '.') . " litros\n";
echo "Custo total da viagem: R$ " . number_format($custoTotal, 2, ',', '.') . "\n";
?>
