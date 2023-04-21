[Repositório do plugin](https://github.com/elias-sundqvist/obsidian-react-components)
[QuickAdd API](https://quickadd.obsidian.guide/docs/QuickAddAPI)
---

> - QuickAdd é um plugin usado para adicionar rapidamente novas páginas e novo conteúdo em seu vault
> - Você pode adicionar notas em pastas específicas do seu vault usando um atalho, preencher o  front matter em YAML usando prompts, etc...

# Opções

- **Template**: é uma definição de como criar uma nova nota e se compõe com o próprio plugin de modelos do Obsidian ou plugins de modelos da comunidade. Por exemplo, isso permitiria definir uma ação rápida para criar uma nova nota em um local específico, com um título padronizado e conteúdo padronizado. Pode ser utilizado em conjunto com o [Templater]()

- **Capture**: permite adicionar rapidamente conteúdo a arquivos predefinidos. Por exemplo, você poderia configurar uma ação rápida para adicionar um link ao arquivo aberto na sua nota diária em uma seção específica.

- **Macros**: permite unir as duas anteriores em fluxos de trabalho encadeados. Pressione uma única tecla de atalho para criar automaticamente uma nova nota de um livro, enquanto adiciona automaticamente uma referência a ela na sua nota de "lista de leituras" e na sua nota diária.

# Como usar

1. Vá em Settings > Community Plugins > QuickAdd > 

<img src="/assets/quickadd-settings.png" width="500px" />

2. Para utilizar os comandos: abra a *Command Palette*(``Crtl+p``/``Cmd+p``) ou use o plugin [Buttons]()

```button
name Adicionar projeto
type command
action QuickAdd: Adicionar projeto
```
<img src="/assets/quickadd-command-palette.png" width="500px" />
