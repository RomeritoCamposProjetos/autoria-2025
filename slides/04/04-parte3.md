---
marp: true
title: CSS — Seletores
description: Tipo, Classe, ID e Atributo
theme: design
footer: '[Autoria Web - Prof. Romerito Campos - 2025](https://rocampos.github.io/)'
_class: lead
size: 16:9
---

# CSS — Combinadores

---

## CSS — Combinadores

- **Combinadores** são usados em CSS para **selecionar elementos com base em sua relação com outros elementos no HTML**.

- Eles permitem escrever seletores mais precisos e contextuais.

---

# Combinador Descendente (`espaco`)

---

<style scoped>
    pre {
        font-size: 20px
    }
</style>

## Combinador Descendente (`espaco`)

Seleciona **todos os elementos descendentes** (em qualquer profundidade) de outro elemento.
**Sintaxe**

```css
elemento descendente {
  propriedade: valor;
}
```
**Exemplo**
Seleciona todos os `<p>` que estão dentro de `<div>`, mesmo se aninhados profundamente.
```css
div p {
  color: blue;
}
```

---


## Combinador Descendente (`espaco`)

**HTML de exemplo**

```html
<div>
  <p>Este parágrafo será azul.</p>
  <section>
    <p>Também ficará azul.</p>
  </section>
</div>
<p>Este parágrafo fora da div não será azul.</p>
```
</div>

- O último parágrafo do código acima não será azul por não ser descendente da `div`
- Os demais são descendentes e terão a regra do slide anterior aplicada

---

# Combinador Filho Direto (`>`)

---

## Combinador Filho Direto (`>`)

Seleciona **somente os filhos diretos** de um elemento.

**Sintaxe**

```css
pai > filho {
  propriedade: valor;
}
```

**Exemplo**

```css
div > p {
  color: blue;
}
```

✔️ Aplica o estilo somente aos `<p>` que são filhos diretos de `<div>`.

---

### HTML de exemplo

```html
<div>
  <p>Direto (colorir de azul)</p>
  <article>    
    <p>
      Filho de filho (não colorir de azul)
    </p>
  </article>
</div>
```

- Apenas o `<p>` que é filho imediado (direto) de div e cnotém o texto `Direto (colorir de azul)` será colorido de azul.

---

# Combinador Irmão Adjacente (`+`)

---
<style scoped>
    pre {
        font-size: 20px
    }
</style>

## Combinador Irmão Adjacente (`+`)

Seleciona **o elemento que vem imediatamente após outro elemento** (mesmo nível, imediatamente depois).

**Sintaxe**

```css
elemento1 + elemento2 {
  propriedade: valor;
}
```
**Exemplo**
Remove o espaçamento **apenas do parágrafo que vem logo depois do h2**.
```css
h1 + p {
  color: grey;
  font-style: italic;
}
```

---

### HTML de exemplo

- Este exemplo utiliza o css definido no slide anterior

```html
<h1>Título</h1>
<p>Este parágrafo é afetado.</p>
<p>Este outro não é afetado.</p>
```
- Apenas o primeiro parágrafo será colorido. Ele é **imediado** ao `<h1>`


---

# Combinador Irmão Geral (`~`)

---
## Combinador Irmão Geral (`~`)

Seleciona **todos os irmãos seguintes** de um elemento (não apenas o próximo imediato).

**Sintaxe**
```css
elemento1 ~ elemento2 {
  propriedade: valor;
}
```

**Exemplo**
Seleciona todos os `<p>` que aparecem depois de `<h2>`, no mesmo nível do DOM.
```css
h2 ~ p {
  color: green;
}
```

---

### HTML de exemplo

- Utiliza o css definido no slide anterior.

```html
<h2>Seção</h2>
<p>Este é afetado (verde).</p>
<p>Este também (verde).</p>
<div>
  <p>Este não é afetado (aninhado).</p>
</div>
```

- Todos os `<p>` no mesmo nível do `<h1>` serão afetados. 
- O `<p>` que está dentro da `div` não está no mesmo nível do `<h2>` e não será afetado. Esse `<p>` não é irmão do `<h1>`

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

## Resumo

| Combinador | Significado               | Exemplo   | Seleciona                                            |
| ---------- | ------------------------- | --------- | ---------------------------------------------------- |
| (espaço)   | Descendentes              | `div p`   | Todos os `<p>` dentro de `<div>`, em qualquer nível. |
| `>`        | Filho direto              | `ul > li` | Apenas `<li>` filhos imediatos de `<ul>`.            |
| `+`        | Irmão adjacente imediato  | `h2 + p`  | `<p>` logo após `<h2>`.                              |
| `~`        | Todos os irmãos seguintes | `h2 ~ p`  | Todos os `<p>` após `<h2>`, no mesmo nível.          |

---

## 🔎 Dica Final

✔️ Combinadores ajudam a criar seletores mais específicos e **evitar classes ou IDs desnecessários**.
✔️ Planeje bem sua estrutura HTML para tirar o máximo proveito dos combinadores!