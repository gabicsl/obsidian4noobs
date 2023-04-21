[Repositório do plugin](https://github.com/shabegom/buttons)

---

> Execute comandos e abra links clicando em ✨ Botões ✨.


# Como criar um botão

1. Abra o *Command Palette* (utilize ``crtl+p``/ ``cmd+p``)
2. Pesquise por *Buttons*, irá aparecer duas opções:

<img src="/assets/buttons-command-palette.png" alt="ícone do obsidian" width="500px" />

## Button Maker
> - É um popup onde você irá criar o botão e configurar ele

<img src="/assets/button-maker.png" alt="ícone do obsidian" width="500px" />

````
```button
name Forum do Obsidian
type link
action https://forum.obsidian.md/
```
````

## Inline button

> - É basicamente uma cópia de um bloco de código de um botão existente, inserido dentro do texto

<img src="/assets/button-inline.png" alt="ícone do obsidian" width="500px" />

Para criar um botão inline:

1. Crie um botão usando o Button Maker ou escreva o código do botão à mão.
2. Certifique-se de que o botão tem um "button-block-id" único.
3. Vá pra nota que você deseja inserir o botão inline e execute o comando "Insert Inline Button" ou escreva o "button-block-id" entre crases

<img src="/assets/button-crase.png" alt="ícone do obsidian" width="200px" />

5. Os "Inline Buttons" devem começar com a palavra "button"



# Utilizando com o plugin QuickAdd

Você pode usar em conjunto com o plugin QuickAdd, por exemplo:

````
```button
name Adicionar projeto
type command
action QuickAdd: Adicionar projeto
```
````

Ao clicar neste botão ele irá executar um comando do [QuickAdd]() pra criar um novo arquivo de projeto usando um template
