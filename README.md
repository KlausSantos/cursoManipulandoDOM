# Curso JavaScript: Manipulando elementos no DOM
### DOM é a sigla para Document Object Model (Modelo de Objeto de Documento)

## Como pegar elementos na Tela
```
document.querySelector('tag_html')
```
### Selecionar uma lista de elementos
```
document.querySelectorAll('tag_html')
```
### além da tag, pode se pegar pela classe ou id

## Outra forma
```
document.getElementsByClassName('nome_classe')
document.getElementsById('nome_id')
```

## Referenciando o arquivo JS na tag head
```
<script src="./script.js" defer></script>
```

## Metodo addEventListener
A sintaxe básica é a seguinte:
```
elemento.addEventListener(evento, callback);
```
#### Onde:

- elemento: É o elemento HTML ao qual queremos associar o evento.
- evento: É uma string que representa o tipo de evento que desejamos capturar.
- callback: É a função que será chamada quando o evento ocorrer.

#### Tipos de Eventos
* _click_
* _submit_
* _keydown, keyup, keypress_
* _focus, blur_

## Metodo classList
O classList é uma propriedade do JavaScript que representa uma lista de classes CSS. Ele fornece métodos que facilitam a adição, remoção e verificação de classes, tornando a manipulação de classes CSS mais eficiente e menos suscetível a erros de programação.
#### Adicionando uma classe
Para adicionar uma classe a um elemento HTML, podemos usar o método add() do classList.
```
const element = document.getElementById('meuElemento');
element.classList.add('minhaClasse');
```
#### Removendo uma classe
Para remover uma classe de um elemento HTML, podemos utilizar o método remove() do classList. 
```
const element = document.getElementById('meuElemento');
element.classList.remove('minhaClasse');
```
#### Alternando uma classe
O método toggle() do classList permite alternar uma classe em um elemento. 
```
const element = document.getElementById('meuElemento');
element.classList.toggle('minhaClasse');
```
#### Verificando se uma classe está presente
Para verificar se uma classe específica está associada a um elemento, podemos usar o método contains() do classList, como no exemplo:
```
const element = document.getElementById('meuElemento');
if (element.classList.contains('minhaClasse')) {
  // A classe 'minhaClasse' está presente no elemento
  // Faça algo aqui...
}
```

## Atributos
* __getAttribute__
O método getAttribute é usado para obter o valor de um atributo específico de um elemento HTML. Ele recebe um argumento, que é o nome do atributo que desejamos recuperar o valor.
```
// HTML: <div id="meuElemento" data-info="Exemplo de atributo">

const elemento = document.getElementById('meuElemento');
const valorDoAtributo = elemento.getAttribute('data-info');
console.log(valorDoAtributo); // Saída: "Exemplo de atributo"
```

* __setAttribute__
O método setAttribute é usado para definir ou modificar o valor de um atributo em um elemento HTML. Ele aceita dois argumentos: o primeiro é o nome do atributo que queremos definir ou modificar, e o segundo é o valor que queremos atribuir a esse atributo. Se o atributo já existir, o método setAttribute irá sobrescrevê-lo; caso contrário, ele criará um novo atributo.
```
// HTML: <p id="meuParagrafo">Texto inicial</p>


const paragrafo = document.getElementById('meuParagrafo');
paragrafo.setAttribute('id', 'paragrafoModificado');
paragrafo.setAttribute('data-novo-atributo', 'Novo valor');
```

* __hasAttribute__
O método hasAttribute é usado para verificar se um elemento possui um atributo específico. Ele recebe um argumento, que é o nome do atributo que queremos verificar. O método retornará true se o atributo existir e false se o atributo não estiver presente.
```
// HTML: <a href="https://www.exemplo.com" id="meuLink">Link de exemplo</a>


const link = document.getElementById('meuLink');
const temHref = link.hasAttribute('href');
console.log(temHref); // Saída: true
const temTarget = link.hasAttribute('target');
console.log(temTarget); // Saída: false
```

* __removeAttribute__
O método removeAttribute é usado para remover um atributo específico de um elemento HTML. Ele recebe um argumento, que é o nome do atributo que desejamos remover.
```
// HTML: <img src="imagem.jpg" alt="Imagem de exemplo" id="minhaImagem">


const imagem = document.getElementById('minhaImagem');
imagem.removeAttribute('alt');
```

## Criando um Objeto ‘Audio’
Para criar um novo objeto ‘Audio’, podemos simplesmente usar a seguinte sintaxe:
```
const audioElement = new Audio('caminho/do/arquivo-de-audio.mp3');
```
#### Controles básicos de áudio
* play(): inicia a reprodução do áudio;
* pause(): pausa a reprodução do áudio;
* currentTime: propriedade que retorna ou define a posição atual de reprodução do áudio, em segundos;
* volume: propriedade que retorna ou define o nível de volume do áudio, variando de 0 a 1.
#### Exemplo de utilização dos métodos do objeto Audio:
```
const audioElement = new Audio('caminho/do/arquivo-de-audio.mp3');

audioElement.play(); // Inicia a reprodução
audioElement.pause(); // Pausa a reprodução
audioElement.currentTime = 10; // Move para 10 segundos no áudio
audioElement.volume = 0.5; // Define o volume para metade (50%)
```