[Repositório do plugin](https://github.com/SilentVoid13/Templater)

---

> - Templater é um plugin de modelo para o Obsidian
> - Ele define uma linguagem de modelo que permite inserir variáveis e resultados de funções em suas notas
> - Ele também permite executar código JavaScript manipulando essas variáveis e funções
> - Desta forma você poderá criar modelos poderosos para automatizar tarefas manuais



1. Configure um pasta para seus templates
2. Vá nas configurações do plugin e coloque o caminho desta pasta de templates
3. Para acionar os templates use o *Command Palette*(``Crtl+p``/``Cmd+p``) e pesquise *Templater*

<img src="/assets/templater-command-palette.png" width="500px" />


# Documentação e sintaxe

https://silentvoid13.github.io/Templater/

# Exemplo

**O seguinte arquivo de template está usando a sintaxe do Templater:**

```
---
data de criação: <% tp.file.creation_date() %>
data de modificação: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---

<< [[<% tp.date.now("YYYY-MM-DD", -1) %>]] | [[<% tp.date.now("YYYY-MM-DD", 1) %>]] >>

# <% tp.file.title %>

<% tp.web.daily_quote() %>
```

**Produzirá o seguinte resultado quando inserido:**
```
---
data de criação: 2021-01-07 17:20
data de modificação: Thursday 7th January 2021 17:20:43
---

<< [[2021-04-08]] | [[2021-04-10]] >>

# Teste Teste

> Alguma frase muito inspiradora

```
