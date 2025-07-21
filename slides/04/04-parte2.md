---
marp: true
title: CSS — Seletores
description: Tipo, Classe, ID e Atributo
theme: design
footer: '[Autoria Web - Prof. Romerito Campos - 2025](https://rocampos.github.io/)'
_class: lead
size: 16:9
---

# CSS — Seletores

---

## CSS — Seletores

- CSS usa **seletores** para escolher quais elementos HTML receberão estilos. 
- Um seletor “aponta” para elementos do DOM para aplicar regras.

---

#  Seletor de Tipo
---
<style scoped>
  pre {
    font-size: 18px
  }
</style>
##  Seletor de Tipo
O **seletor de tipo** seleciona todos os elementos de um determinado nome de tag.

**Sintaxe**
```css
elemento {
  propriedade: valor;
}
```
**Exemplo**
Seleciona **todos os elementos `<p>`** e aplica cor azul e tamanho de 16px.
```css
p {
  color: blue;
  font-size: 16px;
}
```

---

## Dica

* Afeta todos os elementos daquele tipo na página.
* Útil para estilos globais e consistentes.

---
# Seletor de Classe
---
##  Seletor de Classe

Seleciona elementos com um **atributo class** específico.

✔️ Classes são reutilizáveis: vários elementos podem ter a mesma classe.

### Sintaxe

```css
.nome-da-classe {
  propriedade: valor;
}
```

---

### Sintaxe

Utilizando HTML:
```html
<p class="destaque">Este parágrafo está em destaque.</p>
```
Regra definida no CSS:
```css
.destaque {
  color: orange;
  font-weight: bold;
}
```
✔️ Todos os elementos com `class="destaque"` receberão esse estilo.

---

## Dicas sobre Classes

* Use nomes descritivos.
* Um elemento pode ter várias classes.
* Permite **reutilização de estilos**.

---

#  Seletor de ID

---
##  Seletor de ID

Seleciona **um elemento único** com um atributo `id`.

✔️ IDs devem ser **únicos** por página.

### Sintaxe

```css
#nome-do-id {
  propriedade: valor;
}
```

---

### Sintaxe

Utilizando em HTML:

```html
<h1 id="titulo-principal">Bem-vindo!</h1>
```

Regra definida no CSS:

```css
#titulo-principal {
  color: darkred;
  text-align: center;
}
```

---

## Dicas sobre IDs

* Use para **elementos únicos** (ex.: cabeçalhos principais, containers específicos).
* Maior **especificidade** que classes ou tipo.
* Evite usar IDs para estilos reaproveitáveis — prefira classes.

---

# Seletor de Atributo

---
## Seletor de Atributo

Seleciona elementos com **atributos específicos** ou valores de atributos.

### Sintaxe

```css
[atributo] {
  propriedade: valor;
}

[atributo="valor"] {
  propriedade: valor;
}
```

---

## Seletor de Atributo

### Exemplos

#### Selecionar todos os inputs

```css
input {
  border: 1px solid gray;
}
```

#### Selecionar inputs do tipo texto

```css
input[type="text"] {
  border-color: blue;
}
```

---

## Dicas sobre Atributos

* Muito útil para formularios e links.
* Permite estilos contextuais precisos.

---

## Resumo

- **Seletor de Tipo**: Aponta para todas as tags de um tipo (ex.: `p`, `h1`).
- **Seletor de Classe**: Começa com `.` e estiliza qualquer elemento com a classe.
- **Seletor de ID**: Começa com `#`, estiliza um único elemento com esse id.
- **Seletor de Atributo**: Aponta para elementos com atributos ou valores específicos.