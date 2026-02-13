# Como o formulário se posiciona na frente da imagem?

O formulário aparece na frente da imagem de fundo devido ao uso de **flexbox** e ao **gradiente escuro** aplicado à imagem. Aqui está o resumo:

## 1. Estrutura HTML

O formulário está dentro de uma `div` com o **id** `#subscription-form`, que é irmã da `div` com o **id** `#disclaimer`. Ambas estão dentro do `header` com o **id** `#event-subscription`.

```html
<header id="event-subscription">
  <div id="disclaimer">
    <!-- Conteúdo do disclaimer -->
  </div>
  <div id="subscription-form">
    <!-- Formulário -->
  </div>
</header>
```

## 2. Estilização do `#event-subscription`

O `header` tem uma imagem de fundo com um **gradiente escuro** e usa **flexbox** para organizar os elementos internos.

```css
#event-subscription {
  background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), url("../img/moto5.jpg");
  background-position: center;
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: var(--text-color);
  text-align: center;
}
```

### Explicação:
- **`background`**: Define a imagem de fundo com gradiente escuro.
- **`display: flex`**: Organiza os elementos filhos em uma coluna (`flex-direction: column`).

## 3. Estilização do `#subscription-form`

O formulário tem um **fundo cinza claro** e é **centralizado**.

```css
#subscription-form {
  background-color: var(--secondary);
  padding: 2em;
  width: 100%;
  max-width: 400px;
  margin-top: 2em;
}
```

### Explicação:
- **`background-color`**: Define a cor de fundo do formulário.
- **`max-width: 400px`**: Limita a largura do formulário.

## 4. Por que o formulário parece estar na frente?

- A imagem é um **fundo do `header`**.
- O formulário é um **elemento filho** do `header` e é **renderizado acima do fundo**.
- O **gradiente escuro** cria contraste, destacando o formulário.

## 5. Responsividade

Em telas menores, o formulário e o conteúdo do `#disclaimer` são **empilhados verticalmente** (`flex-direction: column`), mantendo a legibilidade.

## 📌 Resumo

O formulário aparece "na frente" da imagem porque:

✅ A imagem é um **fundo do `header`**.  
✅ O formulário é um **elemento filho renderizado acima do fundo**.  
✅ O **gradiente escuro destaca o formulário**.

