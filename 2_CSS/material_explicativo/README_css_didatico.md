# Material CSS — Guia Prático e Didático

Este material foi reorganizado para estudo no VS Code usando **um único `index.html` e um único `style.css`**.

A proposta continua sendo aprender CSS na prática: abrir no navegador, alterar uma propriedade e observar o efeito.

## Arquivos

- `index.html` — conteúdo, exemplos visuais e explicações.
- `style.css` — estilos, comentários e propriedades utilizadas.
- `README.md` — orientação de estudo.

## Como abrir

1. Coloque os arquivos na mesma pasta.
2. Abra a pasta no VS Code.
3. Instale a extensão **Live Server**, caso ainda não tenha.
4. Abra o `index.html` com **Open with Live Server**.
5. Abra também o DevTools do navegador (`F12`).

## Como estudar

Para cada seção:

1. Leia a explicação no HTML.
2. Encontre as classes correspondentes no CSS.
3. Altere **uma propriedade por vez**.
4. Salve.
5. Observe o navegador.
6. Tente prever o resultado antes de fazer a próxima alteração.
7. Use o DevTools para verificar o Box Model e as regras aplicadas.

## Ordem recomendada

### 1. Fundamentos
- seletor
- propriedade
- valor
- declaração
- CSS inline, internal e external
- cascade

### 2. Seletores
- elemento
- classe
- ID
- descendente
- pseudo-classes

### 3. Box Model
- content
- padding
- border
- margin
- width / height
- `box-sizing`
- shorthand
- margin collapse

### 4. Display
- `block`
- `inline`
- `inline-block`
- `none`
- relação com Flexbox e Grid

### 5. Flexbox
- eixo principal
- eixo transversal
- `flex-direction`
- `justify-content`
- `align-items`
- `gap`

### 6. Grid
- linhas
- colunas
- `grid-template-columns`
- `repeat()`
- `fr`
- `gap`

### 7. Position
Esta é uma das partes que merece mais prática:

- `static`
- `relative`
- `absolute`
- `fixed`
- `sticky`
- `top`, `right`, `bottom`, `left`
- fluxo normal
- containing block
- relação pai `relative` + filho `absolute`

### 8. Z-index
- empilhamento
- sobreposição
- stacking context

### 9. Responsividade
- `@media`
- `max-width`
- `min-width`
- unidades relativas
- `clamp()`

## O exercício mais importante de Position

Comece com:

```css
.pai {
    position: relative;
}

.filho {
    position: absolute;
    top: 0;
    right: 0;
}
```

Depois:

1. remova o `position: relative` do pai;
2. observe o resultado;
3. coloque novamente;
4. altere `top`;
5. altere `right`;
6. troque `absolute` por `relative`;
7. compare o fluxo.

## O exercício mais importante de Box Model

Compare:

```css
.box {
    width: 180px;
    padding: 20px;
    border: 5px solid;
}
```

com:

```css
.box {
    box-sizing: border-box;
}
```

Observe no DevTools como o navegador representa **content, padding, border e margin**.

## O exercício mais importante de Flexbox

Altere:

```css
display: flex;
flex-direction: row;
justify-content: space-between;
align-items: center;
gap: 10px;
```

Teste diferentes valores e tente prever a posição dos itens.

## O exercício mais importante de Z-index

Altere os valores:

```css
z-index: 1;
z-index: 5;
z-index: 10;
```

Depois estude o conceito de **stacking context**. O número sozinho não explica todos os casos de sobreposição.

## Outros conceitos incluídos

Além do material original, esta versão inclui exemplos de:

- unidades `px`, `%`, `rem`, `vw`, `vh`;
- `clamp()`;
- Flexbox;
- Grid;
- pseudo-classes `:hover`, `:focus`, `:nth-child()`;
- pseudo-elementos `::before`;
- `overflow`;
- `opacity`;
- `box-shadow`;
- `transform`;
- `transition`;
- Media Queries;
- uso do DevTools.

## Regra de ouro

Não tente decorar todo o CSS.

Quando encontrar uma propriedade nova, pergunte:

> **Qual elemento ela afeta?  
> Em qual contexto ela funciona?  
> Ela altera tamanho, espaço, fluxo, posição, aparência ou layout?**

Depois teste no navegador.
