# Atividade

## **Questão 1 — Introdução ao CSS (inclusão via `<style>`)**

Crie uma página HTML com um título (`<h1>`) e um parágrafo (`<p>`). Use **CSS interno** (dentro da tag `<style>`) para:

* Deixar o título com cor **azul**
* Fazer o parágrafo ter **alinhamento justificado**

## **Questão 2 — Seletor de tipo**

Crie um documento com 3 elementos: `<h2>`, `<p>`, `<ul>`.
Use CSS para aplicar:

* Cor de fundo **amarela** para todos os `<h2>`
* Fonte **itálica** para todos os parágrafos
* Cor do texto da lista (`<ul>`) em **verde**

## **Questão 3 — Seletor de classe**

Crie um CSS que estilize os elementos com a **classe `destaque`**.
No HTML, use essa classe em um `<p>` e em um `<li>`.
Estilo esperado:

* Texto em **negrito**
* Fundo em **cinza-claro**

## **Questão 4 — Seletor de id**

Crie um botão com o `id="enviar"` e um parágrafo com o `id="mensagem"`.
Estilize:

* O botão com cor de fundo **verde** e texto **branco**
* O parágrafo com fonte **tamanho 18px** e cor **azul-marinho**

## **Questão 5 — Seletor de atributo (igualdade)**

Crie três links:

```html
<a href="https://exemplo.com">Exemplo</a>
<a href="mailto:contato@site.com">Email</a>
<a href="https://outro.com">Outro</a>
```

Use um seletor de atributo para aplicar **cor vermelha apenas aos links que começam com `mailto:`**.

## **Questão 6 — Seletor de atributo (valor parcial)**

Crie uma lista com `<li>`s que possuem o atributo `data-tipo`.
Exemplo:

```html
<li data-tipo="urgente">Reunião</li>
<li data-tipo="normal">Estudo</li>
<li data-tipo="urgente">Entrega</li>
```

Use CSS para aplicar:

* Fundo **vermelho-claro** para todos os elementos que têm `data-tipo="urgente"`

Dica: use o seletor `[data-tipo="urgente"]`.