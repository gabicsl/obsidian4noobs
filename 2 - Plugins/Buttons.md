[Repositório do plugin](https://github.com/shabegom/buttons)

---

> Execute comandos e abra links clicando em ✨ Botões ✨.


# Como criar um botão

1. Abra o *Command Palette* (utilize ``crtl+p``/ ``cmd+p``)
2. Pesquise por *Button Maker*


# Botão com link
```button
name Forum do Obsidian
type link
action https://forum.obsidian.md/
```
^button-forum

# Utilizando com o plugin QuickAdd

Você pode usar em conjunto com o plugin QuickAdd, por exemplo:

```button
name Adicionar projeto
type command
action QuickAdd: Adicionar projeto
```

Ao clicar neste botão ele irá executar um comando do [QuickAdd]() pra criar um novo arquivo de projeto usando um template