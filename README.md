# Framework Simulator
Estrutura básica de projetos front-end para estudos de HTML, JS, CSS / SASS. 

- Flexível para você adaptar para projetos e estudos.
- Estensível, você consegue instalar novas bibliotecas e adaptar para outras linguagens.  

## Stack inicial
- Babel
- CSS
- HTML
- JavaScript
- Node / NPM
- Sass
- Webpack

## Instalação
- Requer o node.js instalado
- Baixar ou clonar este repositório
- Acessar com o terminal a pasta do projeto, baixado e **executar o comando**:
```
npm install 
```
## Execução
- Na raiz do projeto, executar o comando:
```
npm run dev
```
<div id="root">
      <h1>Flexbox</h1>
         <h2>Space-around</h2>
        <div class="box_container box_container--around ">
            <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
        </div>
        <h2>Space-between</h2>
        <div class="box_container box_container--between ">
            <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
        </div>
        <h2>Space-evenly</h2>
        <div class="box_container box_container--evenly ">
            <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
        </div>
        <h2>Grid</h2>
        <div class="box_container box_container--grid ">            
            <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
            <div class="box">Box 5</div>
            <div class="box">Box 6</div>
            <div class="box">Box 7</div>
            <div class="box">Box 8</div>
            <div class="box">Box 9</div>
        </div>
        <h2>Center</h2>
        <div class="box_container box_container--center">
           <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
        </div>

        <div class="box_container box_container--image">
            <div class="box" id="building"></div>
            <div class="box" id="dragons"></div>
        </div>
    </div> 

    ## Site para fontes 

    dafont
    css3 genarator

    
     .box_container {
        
          background: $color-bg-boxes;
          display: flex;
          flex-direction: row;
          flex-wrap: wrap;
          justify-content: space-around;
          padding: 1rem;
          max-width: 500px;

           &--around {
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: space-around;
            align-items: stretch;
            
           }

           &--between {
            flex-direction: row-reverse;
            flex-wrap: wrap;
            justify-content: space-between; // eixo x
            align-items: flex-end; // eixo y
           }

           &--evenly {
            flex-direction: row-reverse;
            flex-wrap: wrap;
            justify-content: space-evenly;
            align-items: flex-end;
           }

           &--between {
            flex-direction: row-reverse;
            flex-wrap: nowrap;
            justify-content: center;
           }

           &--grid {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            grid-template-rows: repeat(3, 1fr);
            gap: 1rem;
            height: fit-content;
           }

           &--image {
            .box {
                overflow: hidden;
                border: 3px solid $color-bg-default;
                width: 15rem;
                img {
                    width: 20rem;
                    height: 20rem;
                   object-fit: cover;
                   object-position: 80% 100%;
                }
            }
           }
        }
        

    
        .box {
            background-color: $background-bg-color;
            color: $color-font;
            display: flex;
            border-radius: 1rem;
            align-items: center;
            justify-content: center;
            margin: .5rem;
            position: relative;
            border: 2px solid $color-font;
            min-width: 10rem;
            min-height: 10rem;

            animation-name: slideIn;
            animation-duration: 3s;
            animation-iteration-count: 2;
            animation-direction: alternate;
        }

        @keyframes slideIn {
            from {
                left: -999px;
                opacity: .1;
                height: 0;
                width: 0;
            }

            to {
                left: 0;
                opacity: 1;
                height: fit-content;
            }
        }
        
      