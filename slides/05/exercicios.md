# Lista de Exercícios – Box Model e Position (CSS)

## Parte 1 – Box Model (Fundamentos)

### **1. Caixa de Destaque**

Crie uma `<div>` com um texto de destaque:

```html
<div class="destaque">Promoção válida até amanhã!</div>
```

No CSS:

* Defina largura e altura fixas.
* Aplique `padding` de 20px e `margin` de 15px.
* Dê uma borda de 3px sólida e um `border-radius`.
* Use `box-sizing: border-box` e observe como muda o tamanho total da caixa.

*Pergunta para reflexão:* o que muda se `box-sizing` for `content-box`?

### **2. Caixas Empilhadas**

Crie três `<div>`s (A, B e C) empilhadas verticalmente.

* Dê a cada uma cor diferente.
* Use margens externas diferentes para afastá-las.
* Adicione um `outline` para mostrar onde termina o conteúdo e começa a margem.

*Desafio:* crie um efeito visual de "cartões" com sombra e espaçamento consistente.

## Parte 2 – Position (Conceitos básicos)

### **3. Caixa Relativa**

Crie uma `<div>` com `position: relative` e dentro dela um `<p>` com `position: absolute`.

* Faça o `<p>` ficar preso no **canto inferior direito** da caixa.
* Use `bottom` e `right` para posicionar.
* Dê bordas visuais para entender o espaço ocupado.

*Explique:* por que o elemento absoluto se move dentro do relativo?

### **4. Cabeçalho Fixo**

Crie um cabeçalho (`<header>`) fixo no topo da página com `position: fixed`.

* Dê altura de 80px, cor de fundo e uma sombra.
* Adicione conteúdo abaixo e veja o efeito de sobreposição.
* Use `padding-top` no conteúdo para corrigir o deslocamento.

*Experimente:* o que acontece se o cabeçalho não tiver `width: 100%`?

## Parte 3 – Desafios combinados

### **5. Cartão com Selo de “Novo”**

Monte um bloco representando um produto:

```html
<div class="produto">
  <img src="imagem.jpg" alt="">
  <p>Produto incrível</p>
  <span class="selo">Novo!</span>
</div>
```

CSS:

* Use `position: relative` no `.produto`.
* Coloque o `.selo` com `position: absolute` no **canto superior direito** da imagem.
* Ajuste o `padding`, `margin` e `border` do bloco principal.

*Dica:* adicione `border-radius` e `overflow: hidden` para efeito visual mais limpo.

### **6. Rodapé “grudado” (sticky footer)**

Crie um `<footer>` que:

* Use `position: sticky` com `bottom: 0`.
* Tenha `padding`, `background` e `border-top`.
* Mostre-se apenas quando o usuário rolar até o final da página.

*Dica:* teste com conteúdo longo para ver o comportamento.

### **7. Camadas e Z-index**

Crie três `<div>`s sobrepostas (A, B e C):

* Use `position: absolute` e defina `top` e `left` diferentes.
* Dê cores semi-transparentes e `z-index` distintos.
* Explore a troca das camadas alterando o `z-index`.

*Desafio extra:* adicione uma animação suave de entrada com `transition`.

## Parte 4 – Mini Projeto (para fixar)

Monte um cartaz digital (banner ou card) que combine:

- Um título posicionado com `absolute`.
- Uma imagem central com `box-sizing`: `border-box`.
- Bordas, margens e sombras.
- Um botão fixo de *Comprar* no canto inferior direito da tela.

 *Objetivo:* mostrar domínio visual e técnico do box model + position.

