[Repositório do plugin](https://github.com/elias-sundqvist/obsidian-react-components)

---

# O que é
> É plugin que permite que você escreva e use componentes React com Jsx dentro de suas notas do Obsidian


# Como utilizar

Tem duas formas de criar componentes React no Obsidian:

## 1. Blocos de códigos

> - Coloque uma nota em qualquer lugar do seu vault e coloque a propriedade `defines-react-components`. 
> - Você também pode opcionalmente definir um namespace específico (série de palavras separadas por pontos), usando a propriedade `react-components-namespace`.


1. Você pode colocar no frontmatter, assim:

```
---
defines-react-components: true
react-components-namespace: projects.test
---
```

ou (se o dataview estiver instalado) usando propriedades inline do dataview (Key:: Value)
```
defines-react-components:: true
react-components-namespace:: projects.test
```

Então, em sua nota, para definir um componente, escreva um bloco de código como este:
````
```jsx:component:MyComponent
return <div>Hello {props.name}!</div>
```
````
Isso criará um componente chamado `MyComponent`, localizado no namespace `projetos.teste` (ou no namespace global se você não especificou a propriedade).

Você pode então usar o componente assim:
````
```jsx:
<MyComponent name={"World"}/>
```
````

Ou, usando sintaxe inline.
````
`jsx:<MyComponent name={"World"}/>`
````

Se você estiver em uma nota que usa um namespace separado, pode acessar o componente assim:
````
`jsx:<projects.test.MyComponent name={"World"}/>`
````

## 2. Notas de componentes

Uma maneira alternativa de criar componentes é por meio de notas de componentes. Essa abordagem trata um arquivo markdown inteiro como a definição de um único componente React. Uma vantagem dessa abordagem é que você pode abrir a nota, por exemplo, no VS Code, para obter destaque completo de sintaxe e autocomplete.

Para usar as notas de componente, você primeiro deve especificar uma pasta para as funções Jsx / componentes React.

<img src="/assets/react-components.png" alt="ícone do obsidian" width="500px" />

Cada nota neste diretório será interpretada como o conteúdo de uma função Jsx (implicitamente no formato props=>{seu código aqui}).

Cada arquivo se torna uma função/componente React com o mesmo nome da nota.


# Exemplo de utilização

> Componente de exemplo [Clock](https://github.com/gabibits/obsidian4noobs/blob/master/assets/exemplos/Clock.md)

Uso do component *Clock*:

````
```jsx::Clock
<Clock/>
```
````
