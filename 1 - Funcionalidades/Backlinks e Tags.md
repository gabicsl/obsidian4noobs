# Backlinks

Basicamente "linkar" uma nota a outra nota. É desta forma que são criadas a conexões no [grafo](https://github.com/gabibits/obsidian4noobs/blob/master/1%20-%20Funcionalidades/Grafo%20de%20conhecimento.md). 

> São como as sinapses no nosso cerébro.


Embora o Markdown suporte a criação de links para outras páginas internas ou externas usando seu formato de link, o Obsidian adiciona a ideia de **_backlink_**.

- Os links normais em arquivos markdown são unidirecionais, o que significa que um link aponta apenas para a nova página.
- Os backlinks do Obsidian permitem a criação de links bidirecionais. 
  - Isso significa que, se a página A aponta para a página B, o Obsidian também sabe que a página B está apontando de volta para a página A. Isso permite que as ideias comecem a se ligar enquanto você escreve novas notas, criando um gráfo de notas vinculadas.
- Os backlinks do Obsidian são criados usando o formato de [wikilink](https://en.wikipedia.org/wiki/Help:Link#Wikilinks_(internal_links)) usando colchetes duplos. 


**Aqui está um exemplo de como criar uma nota que se vincula a outra página:**

```markdown
Minha nova nota. Eu quero que essa nota se vincule a [[outra nota]] usando os backlinks do Obsidian.
```

- Por padrão, o Obsidian vinculará a uma nova nota, mas não a criará até que você siga o link. 
- Pressionar `CMD + click` (Mac) ou `CTRL + click` (Windows) no link o levará para uma nova página e a nota será criada em seu vault.

# Tags

Além de vincular notas, o Obsidian permite que você use tags. As tags são outro tipo de link.

- Adicionar tags a uma nota pode torná-las mais fáceis de encontrar em pesquisas se você tiver um grande vault de notas. 
- Elas são úteis para adicionar contexto às suas notas e permitir que você as agrupe. 
- Em seus arquivos Markdown, você adiciona uma nova tag usando um hashtag no estilo do Twitter.

Por exemplo, em meu próprio vault do Obsidian, eu uso `#toread` ou `#towatch` para reunir postagens de blog ou filmes que quero assistir.


```markdown
Uma nota de exemplo. Aqui está uma lista de tags para esta nota: #toread #towatch
```

# Devo usar tags ou links?

Os dois

- Links são conexões de uma nota para outra nota. E como mencionei anteriormente, eles são bidirecionais, então as notas estão vinculadas juntas com um backlink.
- As tags são conexões de uma nota a uma ideia. Uma tag é um link, mas não há nota vinculada a ela.

Então, você realmente não precisa escolher entre links e tags. Por que não usar ambos?

Eu acho que as tags são úteis para agrupar notas e os links são úteis para conectar ideias. Eles são complementares e você pode usá-los juntos.

# Diferença entre tags e links

Embora você possa usar tags e links juntos, há algumas coisas importantes para lembrar.

-   Quando você altera o nome de um arquivo dentro do Obsidian, todos os links para essa pasta serão automaticamente atualizados para apontar para o lugar certo. Isso não acontecerá com as tags.
-   Clicar em uma tag irá abrir uma busca por todos os arquivos que contêm essa tag.
-   Clicar em um link irá abrir a nota vinculada, se ela existir, ou criar uma nova se ela não existir.

[<< Anterior](https://github.com/gabibits/obsidian4noobs/blob/master/1%20-%20Funcionalidades/Pastas%20e%20Notas.md) | [Próxima >>](https://github.com/gabibits/obsidian4noobs/blob/master/1%20-%20Funcionalidades/Grafo%20de%20conhecimento.md)
