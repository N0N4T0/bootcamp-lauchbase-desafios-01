<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Resoluções de Desafios 01
</h3>

<blockquote align="center">“Querer vencer significa já ter percorrido metade do caminho.”</blockquote>

<p align="center">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%23F8952D">
  </a>

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>

</p>

## :rocket: Questões do desafio

### Cálculo de IMC

Crie um programa para calcular o IMC e nível de obesidade de uma pessoa.

A partir desses dados armazene em uma constante chamada `imc` o cálculo do índice de massa corporal definido pela fórmula abaixo:

```js
peso / (altura * altura);
```

Baseado no valor obtido através desse cálculo exiba as seguintes mensagens:

- `SE` o `IMC` maior ou igual a `30`: Carlos você está acima do peso;
- `SE` o `IMC` menor que `29.9`: Carlos você não está acima do peso;

### Cálculo de aposentadoria

Crie um programa para calcular a aposentadoria de uma pessoa.

- O tempo de contribuição mínimo para **homens** é de **35 anos** e, para **mulheres**, **30 anos**;
- Utilizando a regra 85-95, a soma da idade com o tempo de contribuição do **homem** precisa ser de no mínimo 95 anos, enquanto a **mulher** precisa ter no mínimo 85 anos na soma;

Com base nas regras acima imprima na tela as mensagens:

- `SE` a pessoa estiver aposentada: `Silvana, você pode se aposentar!`;
- `SE` a pessoa NÃO estiver aposentada: `Silvana, você ainda não pode se aposentar!`;

### Construção e impressão de objetos

Crie um programa que armazena dados da empresa Rocketseat dentro de um objeto chamado `empresa`. Os dados a serem armazenados são:

Imprima em tela utilizando `console.log` o nome da empresa e seu endereço no seguinte formato:

```
A empresa Rocketseat está localizada em Rua Guilherme Gembala, 260
```

### Vetores e objetos

Crie um programa com um objeto para armazenar dados de um programador como `nome`, `idade` e `tecnologias` que trabalha.

Um programador pode trabalhar com várias tecnologias, por isso armazene essas tecnologias em um array.

Imprima em tela o nome e especialidade da primeira tecnologia que o usuário utiliza no seguinte formato:

```
O usuário Carlos tem 32 anos e usa a tecnologia C++ com especialidade em Desktop
```


# Resolução
```js
// Programa para calcular IMC e nível de obesidade

const nome = 'Lucio'
const peso = 185
const altura = 1.90

const imc = peso / (altura*altura)

if(imc >= 30){
    console.log(`${nome} você está acima do peso. Seu IMC é: ${imc}`)
}
else{
    console.log(`${nome} você não está acima do peso. Seu IMC é: ${imc}`)
}
```

```js
//Programa que calcula a aposentadoria da pessoa

const nome = 'Lucio'
const sexo = 'M'
const idade = 64
const contribuicao = 21

if(sexo === 'F'){
    if(idade+contribuicao >= 85){
        console.log(`${nome}, você pode se aposentar!`)
    }
    else{
        console.log(`${nome}, você não pode se aposentar!`)
    }
} else if(sexo === 'M') {
    if(idade+contribuicao >= 95){
        console.log(`${nome}, você pode se aposentar!`)
    }
    else{
        console.log(`${nome}, você não pode se aposentar!`)
    }
} else{
    console.log('Sexo deve ser M ou F')
}
```

```js
// Programa que armazena dados da empresa Rocketseat em objeto

const empresa = {
    nome: 'Rocketseat',
    cor: 'Roxo',
    foco: 'Programação',
    endereço: {
        rua: 'Rua Guilherme Gembala',
        número: 260,
    } 
};

console.log(`A empresa ${empresa.nome} está localizada em ${empresa.endereço.rua}, ${empresa.endereço.número}`);
```

```js
//Programa com objeto que armazena dados de um programador como
// nome, idade e tecnologias que trabalha

const data = {
    programador: [
        {
            nome: 'Lucio',
            especialidade: "Desktop",
            idade: 34,
            tech1:
                {
                    nome: 'C#, ',
                    info: 'Backend',
                },
            tech2:    
                {
                    nome: 'HTML',
                    info: 'Web',
                },            
        },
        {
            nome: 'Nonato',
            especialidade: "Mobile e Desktop",
            idade: 54,
            techs:[ 
                {
                    nome: 'ReactJS, ',
                    info: 'Frontend Web',
                },
                {
                    nome: 'NodeJS',
                    info: 'Backend',
                }
            ]    
        },
    ]
};

console.log(`O usuário ${data.programador[1].nome} tem ${data.programador[1].idade} anos`)
console.log(`e usa tecnologias como ${data.programador[1].techs[0].nome}${data.programador[1].techs[1].nome}`)
console.log(`com especialidade em ${data.programador[1].especialidade}`)

// console.log(data)

// console.log(data.programador[0].tech1)

// console.log(data.programador[1].techs)
```

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
