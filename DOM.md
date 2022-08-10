# DOM
- Document Object Model
- Estrutura de um arquivo na web
- Representa documentos HTML ou XML
- Interface de programação
- NÃO é linguagem de programação
- É essencial para o JS entender o modelo de páginas web

## Serve para alterar...
##### ... a estrutura
##### ... o estilo
##### ... o conteúdo

## Como?
- Disponibilizando API (Application Programming Interface)
- Rotinas e padrões estabelecidos
- Métodos (funções)
- Árvore de elementos
- Seletores
- Objetos (nós / nodes)

Ao usar F12 em uma página da internet, o navegador utiliza o API fornecido pelo DOM para mostrar o código-fonte da página.
O console/inspetor de cada navegador é diferente por conta das individualidades dos navegadores.

### Exemplo HTML
```
<html> <--- NÓ / NODE
    <head></head> <--- NÓ / NODE>
    <body></body> <--- NÓ / NODE>
</html>
```

### Exemplo Objeto
```
objeto = {
    html : {
        head : {},
        body : {
            h1 : {},
        }
    }
}
```

## DOM x JS 
- O DOM pode ser usado por outras linguagens
- Sem o DOM, o JS não teria como interpretar a página

### Vantagens do JavaScript
- Código é executado por navegadores - diminui o processamento na máquina do programador
- Torna as páginas dinâmicas
- Evita Requisições desnecessárias (melhorando a performance)
- SPA (Single Page Applications)
- Reage rapidamente a ações dos usuários

### Desvantagens do JavaScript
- Código é executado por navegadores - aumenta o processamento na máquina do usuário
- O conteúdo NÃO fica visível para indexadores de busca
- Alterações em tempo de execução não ficam salvas no documento

### Exemplos
Seleciona o objeto e disponibiliza

(métodos / funções).callback

    document.getElementById().innerHTML = ... 
           SELECIONA OBJETO // CALLBACK

- document.getElementById(id)
- document.getElementsByTagName
- document.createElement(name)

- parentNode.appendChild(node) /// html.appendChild('body') ---> insere um node 'body' dentro do html

- element.innerHTML
- element.style
- element.setAttribute()
- element.getAttribute()
- element.addEventListener()
- window.location
- window.onload (en-US)
- window.scrollTo()
- console.log()

Quando há parênteses na expressão após o ponto, está indicando o callback de uma função.
Quando não há, trata-se de callback de uma informação.

## Seletores
- Tipos de seletores: Tag, ID, Class, Name, Query
- Callback
- getElementById() // seletor único
- getElementsByTagName()
- getElementsByName()
- getElementsByClassName()
- querySelectorAll() // #id | .class

### Referências:
- DOM: https://dom.spec.whatwg.org/
- Tecnologias JS: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/JavaScript_technologies_overview
- Motores de execução: https://pt.wikipedia.org/wiki/Lista_de_motores_de_renderiza%C3%A7%C3%A3o
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Regular_Expressions