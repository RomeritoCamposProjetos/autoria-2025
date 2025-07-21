---
marp: true
theme: design
footer: '[Autoria Web - Prof. Romerito Campos - 2025](https://rocampos.github.io/)'
_class: lead
size: 16:9
---

# Introdução ao CSS

---

## Introdução ao CSS

- CSS (Cascading Style Sheets) é uma linguagem usada para **estilizar páginas HTML**. 
- Com CSS você pode controlar cores, fontes, espaçamento, layouts e muito mais.

---

# Inclusão do CSS no HTML

---
## Formas de Inclusão do CSS no HTML

Existem três formas principais de incluir CSS em um documento HTML:

### 1. Inline
O estilo é escrito diretamente no atributo `style` do elemento HTML.
```html
<p style="color: blue; font-size: 16px;">
  Este parágrafo está estilizado inline.
</p>
```
✔️ Vantagem: Simples e rápido para estilos pontuais.
❌ Desvantagem: Difícil de manter em projetos grandes.

---
<style scoped>
  pre {
    font-size: 18px
  }
</style>

### 2. Interno (Embedded)
- O CSS fica no próprio arquivo HTML, dentro da tag `<style>` no `<head>`.
```html
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      color: green;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <p>Este parágrafo usa CSS interno.</p>
</body>
</html>
```
- ✔️ Vantagem: Bom para páginas pequenas ou protótipos.
- ❌ Desvantagem: Código HTML fica maior e menos organizado.
---
### 3. Externo

O CSS fica em um **arquivo separado** (exemplo: `estilos.css`), incluído com `<link>`.

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="estilos.css">
</head>
<body>
  <p>Este parágrafo usa CSS externo.</p>
</body>
</html>
```

---

### 3. Externo

Arquivo `estilos.css`:

```css
p {
  color: red;
  font-size: 20px;
}
```

✔️ Vantagem: Melhor organização, reuso, manutenção.
✅ Forma mais recomendada para projetos reais.

---

# Regras CSS Básicas

---
<style scoped>
  pre {
    font-size: 18px
  }
</style>
## Definição de Regras CSS Básicas

Uma regra CSS tem **seletor** e **declaração(es)**:

```css
seletor {
  propriedade: valor;
  propriedade: valor;
}
```
### Exemplo:

```css
p {
  color: purple;
  font-size: 16px;
}
```

✔️ `p` é o **seletor** (aponta para todos os parágrafos).
✔️ Dentro das chaves `{}` ficam as **declarações** (propriedade e valor).

---

<style scoped>
    table {
      align-self: center;
      justify-self: center;
    }
    table + p {
      font-weight: bolder;
      text-align: center;
      font-size: 20px
    }
</style>

###  Anatomia da Regra


| Parte       | Exemplo  | Descrição                              |
| ----------- | -------- | -------------------------------------- |
| Seletor     | `p`      | Define quais elementos serão afetados. |
| Propriedade | `color`  | O que vai ser modificado.              |
| Valor       | `purple` | Como será modificado.                  |

Resumo dos elementos de uma regra CSS.

---

# Seletores de Tipo

---

## Seletores de Tipo

**Seletores de tipo** (ou element selectors) são os mais básicos. Eles selecionam todos os elementos de um determinado tipo.

### Sintaxe:

```css
elemento {
  propriedade: valor;
}
```
- elemento: pode ser um elemento HTML como `<p>`
- propriedade: por ser algo como `color`
- valor: o valor que é atribuído a propreidade: `blue`

---


### Exemplos:
#### Estilizando todos os parágrafos

```css
p {
  color: darkgreen;
  font-size: 18px;
}
```

#### Estilizando todos os títulos h1

```css
h1 {
  color: navy;
  text-align: center;
}
```
---

##  Dica importante

* Os seletores de tipo afetam **todos os elementos daquele tipo** na página.
* Use com cuidado para evitar alterações indesejadas.

---

##  Resumo
**Formas de inclusão**
* Inline: `style=""` no elemento.
* Interno: `<style>` no `<head>`.
* Externo: arquivo `.css` linkado.

**Regras CSS**
* Seletor + { propriedade: valor; }

**Seletores de tipo**
* Apontam para todos os elementos de um tipo específico (ex: `p`, `h1`, `ul`).