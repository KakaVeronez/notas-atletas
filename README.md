# notas-atletas
let atletas = [
    {
        nome: "Cesar Abascal",
        notas: [10, 9.34, 8.42, 10, 7.88]
    },
    {
        nome: "Fernando Puntel",
        notas: [8, 10, 10, 7, 9.33]
    },
    {
        nome: "Daiane Jelinsky",
        notas: [7, 10, 9.5, 9.5, 8]
    },
    {
        nome: "Bruno Castro",
        notas: [10, 10, 10, 9, 9.5]
    }
];

function calcularMedia(atletas) {
    atletas.forEach(atleta => {
        // Ordenar as notas para identificar a maior e a menor
        atleta.notas.sort((a, b) => a - b);

        // Remover a maior e a menor nota
        let notasValidas = atleta.notas.slice(1, 4);

        // Calcular a média das notas válidas
        let soma = notasValidas.reduce((total, nota) => total + nota, 0);
        let media = soma / notasValidas.length;

        console.log(`Atleta: ${atleta.nome}`);
        console.log(`Notas Obtidas: ${atleta.notas.join(',')}`);
        console.log(`Média Válida: ${media}`);
    });
}

calcularMedia(atletas);
