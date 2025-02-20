# Roteiro de Aula Prática - Algoritmos em JavaScript

## Introdução

### O que são Algoritmos?
Antes de iniciarmos a programação propriamente dita, é importante entendermos o conceito de **algoritmos**. Um algoritmo nada mais é do que uma sequência de passos bem definidos para resolver um problema. Em nosso dia a dia, seguimos diversos algoritmos sem perceber, como por exemplo:
- Uma receita de bolo (passo a passo para preparar um bolo).
- Um manual de montagem de um móvel.
- As instruções para atravessar a rua com segurança.

Na programação, os algoritmos são essenciais, pois definem a forma como os programas resolvem problemas. E hoje vamos explorar alguns algoritmos simples utilizando JavaScript!

Além disso, vamos estruturar nosso código utilizando **funções**, um conceito fundamental na programação. Funções nos permitem reutilizar código e tornar os programas mais organizados e eficientes.

---

## Estruturando o Código em Arquivos HTML e JavaScript
Para melhor organizar nosso código, vamos separar a parte visual (HTML) da parte lógica (JavaScript). No HTML, teremos botões para chamar cada função e exibir os resultados no navegador.

### Estrutura dos arquivos:
1. **index.html** - Contém a interface e os botões.
2. **script.js** - Contém a lógica dos exercícios.

---

## Criando o Arquivo `index.html`
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Algoritmos em JavaScript</title>
</head>
<body>
    <h1>Exercícios de Algoritmos</h1>
    <button onclick="calcularMedia()">Calcular Média</button>
    <button onclick="verificarParOuImpar()">Verificar Par ou Ímpar</button>
    <button onclick="somarNumerosPares()">Somar Números Pares</button>
    <button onclick="calcularFatorial()">Calcular Fatorial</button>
    <button onclick="diaDaSemana()">Converter Número para Dia da Semana</button>
    <button onclick="imprimirPares100()">Imprimir Números Pares (1 a 100)</button>
    <button onclick="alunosAcimaMedia()">Alunos Acima da Média</button>
    <button onclick="multiplicarVetorEscalar()">Multiplicar Vetor por Escalar</button>
    <script src="script.js"></script>
</body>
</html>
```

---

## Criando o Arquivo `script.js`

### Exercício 5: Converter Número para Dia da Semana
**Enunciado:** Desenvolver um algoritmo para ler o número do dia da semana e imprimir o seu respectivo nome por extenso. Caso o número esteja fora do intervalo 1 a 7, exibir a mensagem "Dia da semana inválido".

```javascript
function diaDaSemana() {
    let dia = parseInt(prompt("Digite um número de 1 a 7 para saber o dia da semana: "));
    let diasSemana = ["Domingo", "Segunda-feira", "Terça-feira", "Quarta-feira", "Quinta-feira", "Sexta-feira", "Sábado"];
    if (dia >= 1 && dia <= 7) {
        alert("O dia " + dia + " corresponde a " + diasSemana[dia - 1]);
    } else {
        alert("Dia da semana inválido");
    }
}
```

---

### Exercício 6: Imprimir Números Pares de 1 a 100
**Enunciado:** Fazer um algoritmo que imprima todos os números pares no intervalo de 1 a 100.

```javascript
function imprimirPares100() {
    let resultado = "Números pares de 1 a 100:\n";
    for (let i = 1; i <= 100; i++) {
        if (i % 2 === 0) {
            resultado += i + " ";
        }
    }
    alert(resultado);
}
```

---

### Exercício 7: Alunos com Idade Acima da Média
**Enunciado:** Dada uma tabela contendo a idade de 10 alunos, faça um algoritmo que calcule o número de alunos com idade superior à média.

```javascript
function alunosAcimaMedia() {
    let idades = [15, 18, 20, 22, 24, 30, 17, 19, 21, 25];
    let soma = idades.reduce((acc, idade) => acc + idade, 0);
    let media = soma / idades.length;
    let acimaMedia = idades.filter(idade => idade > media);
    alert("Número de alunos com idade acima da média: " + acimaMedia.length);
}
```

---

### Exercício 8: Multiplicação de Vetor por Escalar
**Enunciado:** Desenvolva um programa que leia um vetor de números reais e um escalar, e imprima o resultado da multiplicação do vetor pelo escalar.

```javascript
function multiplicarVetorEscalar() {
    let vetor = [2.5, 3.7, 4.1, 5.6];
    let escalar = parseFloat(prompt("Digite um número escalar: "));
    let resultado = vetor.map(num => num * escalar);
    alert("Resultado da multiplicação: " + resultado.join(", "));
}
```

---

Com isso, os exercícios estão completos, com explicações detalhadas e exemplos práticos! 🚀

