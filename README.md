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



## Alterando atributos de um elemento
```
variavel.setAttribute('elemento_que_vai_ser_alterado', 'alteracao')


