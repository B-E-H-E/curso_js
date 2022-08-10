# Operadores

## Aritméticos
- Retornam o resultado de uma operação matemática

Somar             +
Subtrair          -
Dividir           /
Multiplicar       *
Resto de divisão  %

## Comparadores Matemáticos
- Testes lógicos, resultados booleano (true/false)

Maior que        >=
Menor que        <=
Maior ou igual a >=
Menor ou igual a <=

## Comparadores Lógicos
- Testes lógicos, resultados booleanos

 ==    igualdade entre sentenças (valor)
 !=    diferença entre sentenças (valor)
 ===   igualdade entre sentenças (valor e tipo)
 !==   diferença entre sentenças (valor e tipo)

## Operadores de Lógica e Junção Lógica
!  NÃO (not)
&& E (and)
|| OU (or)

O sinal de exclamação (!) é utilizado para negar a sententça que vem na sequência.

### Exemplos:
a != b      "o valor de a é diferente do de b"
x !== y     "o valor e o tipo de x são diferentes dos de y"
!a == b     "o valor de a não é igual ao de b"

#### Obs: As condições lógicas são convertidas em números binários:
true = 1
false = 0

## Operadores Lógicos de Atribuição
Atribui valor a uma variável a partir de uma condição lógica (economiza if's e else's)

var minhaCor = cor == "preto" ? "preto" : "branco";

##  If ... Else...

if (cor == "preto") {
    minhaCor = "preto";
} else if (cor == "cinza") {
    minhaCor = "cinza";
} else if (cor == "vermelho") {
    minhaCor = "vermelho";
} else {
    minhaCor = "branco";
}

## Switch

switch (cor) {
    case 'preto' :
        minhaCor = 'preto';
        break;
    case 'cinza' :
        minhaCor = 'cinza';
        break;
    case 'vermelho' :
        minhaCor = 'vermelho';
        break;
    default :
        minhaCor = 'branco'
        console.log('A cor é branco')
}

## Laços de Repetição / Repetition Loops
### for()

for ([expressaoInicial]; [condicao]; [incremento])

### while()
while ([condicao]) {
    [execucao]
}

##### também pode ser usado da forma:
do {
    [execucao]
} while ([condicao])

#### Exemplo for(): Cálculo de média escolar de alunos

var alunos = [
    [6, 7, 8],
    [9, 4, 8],
    [5, 5, 7]
]

var nota = 0;

for (var i = 0; i < alunos.length; i++) {
    nota = 0;
    aluno = alunos[i];
    console.log("Aluno: " + aluno);

    for (c = 0; c < aluno.length; c++) {
        nota += aluno[c];
    }

    media = nota / 3

    if(media >= 7) {
        resultado = "aprovado";
    } else {
        resultado = "reprovado";
    }

    console.log("Média " + media + " - " + resultado);
}

#### Exemplo while(): Contador simples

var contador = 0;

while (contador <= 10) {
    console.log("O termo do contador é " + contador);
    contador++;
}

# Funções

- Evitar repetições de códigos.
- Realizar chamadas dinâmicas de algoritmos.

function myFunction(parametros) {
    
}

### Exemplo - cálculo de média de notas:

function calcularMedia(notas) {

	var somaNotas = 0;
	for (c = 0; c < notas.length; c++) {
	somaNotas += notas[c];
	}
  
  media = somaNotas / notas.length;
  return media;
}

function aprovacao(notas) {

	let media = calcularMedia(notas);
	let condicao = media >= 7 ? "aprovado" : "reprovado";	
  return 'Média: ' + media + ' - Aluno ' + condicao;
}

console.log(aprovacao([10, 8, 6]))

console.log(aprovacao([5, 4, 7]))

## Formulários
- Precisamos evitar que o usuário passe dados incorretos
- Ou seja: direcionar o melhor uso do sistema
-  Proteger a injeção de código malicioso
- Evitar erros de processamento
- Formatar dados para facilitar processamento
- Regex -> expressões regulares