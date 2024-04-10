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
