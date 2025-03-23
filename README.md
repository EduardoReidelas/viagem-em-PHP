# viagem-em-PHP

<?php
// Função para obter um número do usuário
function obterEntrada($prompt) {
    echo $prompt;
    return trim(fgets(STDIN));
}

// Solicita os dados ao usuário
$distancia = obterEntrada("Digite a distância da viagem (em km): ");
$consumo = obterEntrada("Digite o consumo do carro (km por litro): ");
$precoCombustivel = obterEntrada("Digite o preço do combustível (R$ por litro): ");

// Converte as entradas para números
$distancia = (float)$distancia;
$consumo = (float)$consumo;
$precoCombustivel = (float)$precoCombustivel;

// Calcula a quantidade de litros necessários
$litrosNecessarios = $distancia / $consumo;

// Calcula o custo total da viagem
$custoTotal = $litrosNecessarios * $precoCombustivel;

// Exibe os resultados
echo "\nResultado do Cálculo:\n";
echo "Distância da viagem: " . $distancia . " km\n";
echo "Consumo do carro: " . $consumo . " km/l\n";
echo "Preço do combustível: R$ " . number_format($precoCombustivel, 2, ',', '.') . " por litro\n";
echo "Litros necessários para a viagem: " . number_format($litrosNecessarios, 2, ',', '.') . " litros\n";
echo "Custo total da viagem: R$ " . number_format($custoTotal, 2, ',', '.') . "\n";
?>
