# Projeto de Carrossel em JavaScript

[<img src="./\src\imagens/tela-readme.gif" target="_blank">](https://github.com/vandesonsantos/portfolio) 

## Bem-Vindos! 👋

Este é um projeto de carrossel em JavaScript que permite uma navegação dinâmica e interativa entre várias imagens. Com esse carrossel, os usuários podem deslizar suavemente pelas imagens, explorando uma coleção de forma intuitiva. Além disso, o projeto é altamente personalizável, permitindo ajustes como velocidade de transição, exibição automática e controles de navegação. Com uma implementação limpa e de fácil compreensão, esse carrossel é uma ótima adição para sites que desejam exibir imagens de forma atrativa e envolvente.


## Funcionalidades
- Navegação por meio de botões ou gestos de arrastar.
- Suporte a imagens de diferentes tamanhos.
- Controle de velocidade e transição das imagens.


## Tecnologias Utilizadas
- Marcação HTML5 semântica
- Propriedades personalizadas CSS
- Flexbox
- JavaScript

## Como utilizar
Para utilizar este projeto, basta baixar os arquivos do repositório e adicioná-los ao seu projeto. Em seguida, inclua o arquivo JavaScript e o arquivo CSS em seu HTML:

```
<link rel="stylesheet" href="style.css">
<script src="index.js"></script>
```
Em seguida, adicione as imagens que deseja exibir no carrossel no elemento ```<div class="img-carousel"></div>```

```
<div class="img-carousel">
    <img class="imagem ativa" src="./src/imagens/imagem-01-personagens.jpg" alt="Personagens Dragon Ball"/>

    <img class="imagem" src="./src/imagens/imagem-02-guku.jpg" alt="Guku"/>

    <img class="imagem" src="./src/imagens/imagem-03-vegeta.jpg" alt="imagem-03-vegeta"/>

    <img class="imagem" src="./src/imagens/imagem-04-personagens.jpg" alt="Personagens Dragon Ball"/>

    <img class="imagem" src="./src/imagens/imagem-05-personagens.jpeg" alt="Personagens Dragon Ball"/>

    <img class="imagem" src="./src/imagens/imagem-06-personagens.jpg" alt="Personagens Dragon Ball"/>
  </div>
</div>
```

Logo depois, adicione os botões que irá exibir a animação de click na tela com a troca das imagens no carrossel dentro de outro elemento ```<div class="botoes-carrossel"></div>```

```
<div class="botoes-carrossel">
    <button class="botao selecionado"></button>
    <button class="botao"></button>
    <button class="botao"></button>
    <button class="botao"></button>
    <button class="botao"></button>
    <button class="botao"></button>
</div>
```

Por fim, inicialize o carrossel em seu arquivo JavaScript com o seguinte código:

```
const botoesCarrossel = document.querySelectorAll('.botao');
const imagens = document.querySelectorAll('.imagem')

botoesCarrossel.forEach((botao, indice) => {
    botao.addEventListener('click', () => {
    
        const botaoSelecionado = document.querySelector('.selecionado')
        botaoSelecionado.classList.remove('selecionado')

        botao.classList.add('selecionado')

        const imagemAtiva = document.querySelector('.ativa')
        imagemAtiva.classList.remove('ativa')
 
        imagens[indice].classList.add('ativa')
    })
})
```

Pronto! Seu carrossel estará funcionando. Caso queira customizar ainda mais o visual ou comportamento do carrossel, confira os arquivos index.js e style.css e faça suas alterações.

## Veja o Projeto Online
Deploy Do Projeto
- [GitHub Pages](https://vandesonsantos.github.io/carrossel-imagens-dragon-ball/)  


**Divirta-se!** 🚀
