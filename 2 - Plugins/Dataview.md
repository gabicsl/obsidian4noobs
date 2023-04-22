[Repositório do plugin](https://github.com/blacksmithgu/obsidian-dataview)

---

> - Trate seu Vault Obsidian como um banco de dados que você pode consultar
> - Fornece uma API JavaScript e uma linguagem de consulta baseada em pipeline para filtrar, classificar e extrair dados de páginas Markdown

# Como utilizar

Para uma descrição completa de todos os recursos, instruções e exemplos, consulte a [referência](https://blacksmithgu.github.io/obsidian-dataview/).

Para um esboço mais breve, vamos examinar as duas principais áreas do Dataview: _data_ e _querying_

# Data

O Dataview gera dados do seu Vault ao extrair informações do **frontmatter do Markdown** e dos **campos inline**.

-   O frontmatter do Markdown é um YAML incluído entre `---` no topo de um documento Markdown, que pode armazenar metadados sobre aquele documento
-   Os campos inline são um recurso do Dataview que permitem que você escreva metadados diretamente no seu documento Markdown usando a sintaxe `Key:: Value`

**Exemplos de ambos abaixo:**

```
---
type: projeto
tarefasCompletas: 5
totalTarefas: 20
---
```

ou 

```md
# Arquivo Markdown

Livro:: [[Orgulho e Preconceito]]
Autor:: Jane Austen
```


# Querying

Depois de anotar documentos e outros itens com metadados, você pode consultá-los usando qualquer um dos quatro modos de consulta do Dataview:

1.  **Dataview Query Language (DQL)**: Uma linguagem de expressão baseada em pipeline, vagamente semelhante ao SQL, que pode lidar com casos de uso básicos. Consulte a [documentação](https://blacksmithgu.github.io/obsidian-dataview/query/queries/) para mais detalhes.
    
````
```dataview
 TABLE file.name AS "Arquivo", rating AS "Nota" FROM #livro
```
````
    
2.  **Inline Expressions**: Expressões DQL que você pode inserir diretamente em Markdown e que serão avaliadas no modo de visualização. Consulte a [documentação](https://blacksmithgu.github.io/obsidian-dataview/reference/expressions/) para consultas permitidas.

````
``` 
   We are on page `= this.file.name`
 ```
````

3.  **DataviewJS**: Uma API JavaScript de alto nível que dá acesso completo ao índice do Dataview e algumas utilidades convenientes de renderização. Altamente recomendado se você conhece JavaScript, pois é muito mais poderoso que a linguagem de consulta. Verifique a [documentação](https://blacksmithgu.github.io/obsidian-dataview/api/intro/) para mais detalhes.
    
````
 ```dataviewjs
    dv.taskList(dv.pages().file.tasks.where(t => !t.completed));
 ```
````
    
4.  **Inline JS Expressions**: O equivalente em JavaScript às expressões inline, que permitem que você execute qualquer código JS inline:
````
```
This page was last modified at `$= dv.current().file.mtime`.
```
````

# Exemplo

Mostrar todos projetos na pasta projetos e alguns metadados
````
```dataview
TABLE without id file.link as Projeto, length(file.tasks.text) as Total, length(filter(file.tasks.completed, (t) => t = true)) AS Concluído, "<progress value='" + (length(filter(file.tasks.completed, (t) => t = true)) / length(file.tasks.text)) * 100 + "' max='100'></progress>" AS Progresso, status
FROM "projetos"
WHERE file.tasks
sort file.name asc
```
````
<img src="/assets/dataview-projetos.png" width="500px" />
