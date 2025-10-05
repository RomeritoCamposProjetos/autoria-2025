# Código do desafio


## HTML

```html
<div class="container">
    <div class="icon">
        <span class="notification">
            500000
        </span>
        <img src="./whasapp.png" alt="">
    </div>
</div>
```

## CSS

```css
* {
    box-sizing: border-box;
}

body {
    height: 100vh;
}

div.container {
    display: flex;
    flex-flow: column nowrap;
    height: 100%;
    margin: 0 25%;
    align-items: center;
    justify-content: center;
}

.icon {
    background-color: greenyellow;
    block-size: 100px;
    inline-size: 100px;
    padding: 10px;
    border-radius: 15px;
    position: relative;
}

.icon img {
    block-size: 100%;         
}

.notification {
    display: inline-block;
    position: absolute;
    background-color: red;
    border-radius: 20px;
    padding: 0.2em 0.3em;
    color: white;
    top: -0.7em;
    right: -0.7em;
    height: 1.5em;
    writing-mode: horizontal-tb;
    max-width: 100px;    
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow-y: clip;     
}
```