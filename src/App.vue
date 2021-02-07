<template>
<div id="app">
    <header>
        <div class="container">
            <button id="logo" @click="moveScreen('start')"> P0sseid0n </button>
            <nav>
                <h1 @click="viewMenu()">
                    <span v-if="showMenu"><font-awesome-icon :icon="['fas', 'times']"/></span>
                    <span v-else><font-awesome-icon :icon="['fas', 'bars']"/></span>
                </h1>
                <ul :class="{ 'show': (showMenu)  }">
                    <li><button @click="moveScreen('projects')">Projetos</button></li>
                    <li><button @click="moveScreen('knowledge')">Conhecimentos</button></li>
                    <li><button @click="moveScreen('about')">Sobre mim</button></li>
                    <li><button @click="moveScreen('contact')">Contato</button></li>
                </ul>
            </nav>
        </div>
    </header>
    <main id="start">
        <p>Olá, eu sou o</p> 
        <h1 @mouseenter="changeName()" @click="changeName()" > {{ nameDisplay }} <span>&#95;</span> </h1>
        <br>
        <a href="https://github.com/P0sseid0n" target="_blank" rel="noopener noreferrer">
            <font-awesome-icon :icon="['fab', 'github']"/> Meu GitHub
        </a>
        <h2>
            <font-awesome-icon :icon="['fas', 'chevron-down']"/>
        </h2>
    </main>
    <section id="projects">
        <div class="container">
            <h1>Projetos</h1>
            <div class="project">
                <img src="https://s3.imgcdn.dev/CuCza.png" alt="N Words">
                <div class="text">
                    <h1>N words</h1>
                    <p>Contador de letras, palavras e linhas de um texto.</p>
                    <p>Feito em <b>VueJS</b> com <b>HTML</b>, <b>CSS</b> e <b>Javascript</b>.</p>
                    <div class="links">
                        <a href="https://n-words.netlify.app/" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fas', 'link']"/> Website
                        </a>
                        <a href="https://github.com/P0sseid0n/N-Words" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fab', 'github']"/> Github
                        </a>
                    </div>
                </div>
            </div>
            <div class="project rev">
                <img src="https://s3.imgcdn.dev/Cu4ML.png" alt="Mini Loja">
                <div class="text">
                    <h1>Mini loja</h1>
                    <p>Site simulando uma mini loja com sistema de carrinho.</p>
                    <p>Feito em <b>HTML</b> e <b>CSS</b>.</p>
                    <div class="links">
                        <a href="https://miniloja-posseidon.netlify.app/" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fas', 'link']"/> Website
                        </a>
                        <a href="https://github.com/P0sseid0n/Projeto-MiniLoja" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fab', 'github']"/> Github
                        </a>
                    </div>
                </div>
            </div>
            <div class="project">
                <img src="https://s3.imgcdn.dev/CuItw.png" alt="Site comercial">
                <div class="text">
                    <h1>Template de site comercial</h1>
                    <p>Template com base em sites comerciais, site de produtos...</p>
                    <p>Feito em <b>HTML</b> e <b>CSS</b>.</p>
                    <div class="links">
                        <a href="https://paginacomercial01.netlify.app/" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fas', 'link']"/> Website
                        </a>
                        <a href="https://github.com/P0sseid0n/Pagina-Comercial-01" target="_blank" rel="noopener noreferrer">
                            <font-awesome-icon :icon="['fab', 'github']"/> Github
                        </a>
                    </div>
                </div>
            </div>
            <a href="https://github.com/P0sseid0n?tab=repositories" target="_blank" rel="noopener noreferrer" id="more">Ver mais projetos.</a>
        </div>
    </section>
    <section id="knowledge">
        <div class="container">
            <h1>Conhecimentos</h1>
            <div>
                <div class="icon">
                    <img src="https://img.icons8.com/ios-filled/64/3498db/html-5.png"/>
                    <h2>HTML</h2>
                </div>
                <div class="icon">
                    <img src="https://img.icons8.com/ios-filled/64/3498db/css3.png"/>
                    <h2>CSS</h2>
                </div>
                <div class="icon">
                    <img src="https://img.icons8.com/ios-filled/64/3498db/javascript.png"/>
                    <h2>Javascript</h2>
                </div>
                <div class="icon">
                    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                width="64" height="64"
                viewBox="0 0 172 172"
                style=" fill:#000000;"><g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g><path d="M150.5,132.58333c0,9.89717 -8.0195,17.91667 -17.91667,17.91667h-93.16667c-9.89358,0 -17.91667,-8.0195 -17.91667,-17.91667v-93.16667c0,-9.89717 8.02308,-17.91667 17.91667,-17.91667h93.16667c9.89717,0 17.91667,8.0195 17.91667,17.91667z" fill="#3498db"></path><path d="M118.3575,91.73333c-2.32917,-3.225 -5.6975,-5.44667 -10.03333,-6.62917c0,0 3.655,-1.32583 6.95167,-6.27083c1.97083,-3.15333 2.97417,-6.95167 2.97417,-11.395c0,-7.70417 -2.795,-13.61667 -8.385,-17.66583c-5.59,-4.04917 -11.89667,-6.7725 -22.61083,-6.7725h-33.50417v86h37.37417c10.14083,-0.07167 17.77333,-2.2575 22.96917,-6.45c5.16,-4.26417 7.74,-10.57083 7.74,-18.99167c0,-4.65833 -1.14667,-8.6 -3.47583,-11.825zM75.25,57.33333c0,0 14.9425,0 15.22917,0c5.44667,0 9.85417,4.4075 9.85417,9.85417c0,5.44667 -4.4075,9.85417 -9.85417,9.85417c-0.28667,0 -15.22917,0 -15.22917,0zM93.16667,114.66667h-17.91667v-21.5h17.91667c5.94833,0 10.75,4.80167 10.75,10.75c0,5.94833 -4.80167,10.75 -10.75,10.75z" fill="#ffffff"></path></g></g></svg>
                    <h2>Bootstrap</h2>
                </div>
                <div class="icon">
                    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                width="64" height="64"
                viewBox="0 0 172 172"
                style=" fill:#000000;"><g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g><path d="M85.95342,60.91667l-18.82325,-32.25h-56.47333l75.29658,129l75.29658,-129h-56.47333z" fill="#3498db"></path><path d="M104.77667,28.66667l-18.82325,32.25l-18.82325,-32.25h-27.19033l46.01358,78.83333l46.01358,-78.83333z" fill="#455a64"></path></g></g></svg>
                <h2>VueJs</h2>
                </div>
                <div class="icon">
                    <img src="https://img.icons8.com/windows/64/3498db/node-js.png"/>
                    <h2>Node.js</h2>
                </div>
                <div class="icon">
                    <img src="https://img.icons8.com/ios/64/3498db/mysql-logo.png"/>
                    <h2>MySQL</h2>
                </div>
                
                <div class="icon">
                    <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
                width="64" height="64"
                viewBox="0 0 172 172"
                style=" fill:#000000;"><g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g><path d="M150.5,61.99167c0,73.45833 -64.5,95.675 -64.5,95.675c0,0 -64.5,-22.21667 -64.5,-95.675c0,-8.95833 0.71667,-16.48333 1.43333,-22.575c1.075,-8.95833 7.16667,-16.125 15.76667,-18.275c11.10833,-3.225 28.66667,-6.80833 47.3,-6.80833c18.63333,0 36.19167,3.58333 47.65833,6.80833c8.6,2.15 14.69167,9.675 15.76667,18.275c0.35833,6.09167 1.075,13.975 1.075,22.575z" fill="#344a59"></path><path d="M86,25.08333c17.55833,0 34.04167,3.58333 44.79167,6.45c4.3,1.075 7.16667,4.65833 7.88333,9.31667c0.71667,6.80833 1.075,13.975 1.075,21.14167c0,55.9 -41.20833,78.475 -53.75,83.85c-12.54167,-5.73333 -53.75,-28.30833 -53.75,-83.85c0,-7.16667 0.35833,-14.33333 1.075,-21.14167c0.35833,-4.65833 3.58333,-8.24167 7.88333,-9.31667c10.75,-2.86667 27.23333,-6.45 44.79167,-6.45M86,14.33333c-18.63333,0 -36.19167,3.58333 -47.65833,6.80833c-8.24167,2.15 -14.69167,9.675 -15.40833,18.275c-0.71667,6.09167 -1.43333,13.975 -1.43333,22.575c0,73.45833 64.5,95.675 64.5,95.675c0,0 64.5,-22.21667 64.5,-95.675c0,-8.95833 -0.71667,-16.48333 -1.43333,-22.575c-1.075,-8.95833 -7.16667,-16.125 -15.76667,-18.275c-11.10833,-3.225 -28.66667,-6.80833 -47.3,-6.80833z" fill="#3498db"></path><path d="M82.41667,100.33333h7.16667v28.66667h-7.16667z" fill="#c4deef"></path><path d="M86,35.83333c0,0 -21.5,17.91667 -21.5,46.58333c0,18.63333 11.825,30.45833 17.91667,35.83333l3.58333,-10.75l3.58333,10.75c6.09167,-5.375 17.91667,-17.2 17.91667,-35.83333c0,-28.66667 -21.5,-46.58333 -21.5,-46.58333z" fill="#3498db"></path><path d="M86,35.83333c0,0 -21.5,17.91667 -21.5,46.58333c0,18.63333 11.825,30.45833 17.91667,35.83333l3.58333,-10.75z" fill="#71bbed"></path></g></g></svg>
                <h2>MongoDB</h2>
                </div>
            </div>
        </div>
    </section>
    <section id="about">
        <div class="container">
            <h1>Sobre mim</h1>
            <p>Meu nome é Matheus, porém meu apelido na internet é P0sseid0n, tenho 16 anos, moro no Rio de Janeiro, Brasil.</p>
            <p>Estou estudando programação full-stack focado na web com <b>javascript</b>. Comecei estudar programação web em poucos meses então não possuo muitos projetos completos mas estudo todos os dias para sempre melhorar e aumentar essa lista.</p>
            <p>A minha história na programação é bem curta e com varias pausas por desanimo. Faz muito tempo desde que descobri que gostava de programar mas sempre que eu começava estudar eu parava após alguns dias. O meu primeiro curso foi o do <b>Curso em vídeo</b> porém sempre parava, mas após varias tentantivas terminei o curso de <b>javascript</b> no ultimo ano e pretendo fazer o de <b>python</b> em alguns meses.</p>
            <p>Antes de ir para a programação web eu gostava de fazer jogos e para fazer eu usava uma game engine visual chamada <b>Construct</b> porém desanimei. Até então venho estudando todos os dias <b>javascript</b> e novas tecnologias como <b>VueJs</b> para sempre melhorar.</p>
        </div>
    </section>
    <section id="contact">
        <div class="container">
            <h1>Contato</h1>
            <a href="mailto:posseidonking@hotmail.com" target="_blank" rel="noopener noreferrer" title="Email"> <font-awesome-icon :icon="['fas', 'envelope']"/></a>
            <a href="https://github.com/P0sseid0n" target="_blank" rel="noopener noreferrer" title="Github"> <font-awesome-icon :icon="['fab', 'github-square']"/></a>
            <a href="https://discord.com/users/237313382657687552" target="_blank" rel="noopener noreferrer" title="Discord"> <font-awesome-icon :icon="['fab', 'discord']"/></a>
            <a href="https://twitter.com/P0sseid0n" target="_blank" rel="noopener noreferrer" title="Twitter"> <font-awesome-icon :icon="['fab', 'twitter-square']"/></a>
        </div>
    </section>
    <footer>
        <button @click="moveScreen('start')">
            <font-awesome-icon :icon="['fas', 'arrow-up']"/> Ir para o topo <font-awesome-icon :icon="['fas', 'arrow-up']"/>
        </button>
        <hr>
        <h3>Feito por P0sseid0n&#169;</h3>
    </footer>
</div>
</template>

<script>
export default {
    name: 'App',
    data(){
        return{
            name: 'P0sseid0n',
            nameDisplay: 'P0sseid0n',
            showMenu: false,
            scrollY: 0,
            scrollTarget: 0,
            scrolling: ''
        }
    },
    methods:{
        changeName(){
            if(this.nameDisplay != this.name) return
            let deleting = true

            if(this.name == 'P0sseid0n') this.name = 'Matheus'
            else this.name = 'P0sseid0n'

            const typing = setInterval(() => {
                if(this.nameDisplay.length <= 0) deleting = false

                if(deleting){
                    this.nameDisplay = this.nameDisplay.slice(0, this.nameDisplay.length - 1 )
                } else {
                    this.nameDisplay = this.name.slice(0, this.nameDisplay.length + 1 )
                }
                if(this.nameDisplay == this.name) clearInterval(typing)
            }, 150)
        },

        moveScreen(btn){
            if(this.scrolling) return
            let scrollY = window.scrollY || window.screenTop
            let scrollTarget = document.getElementById(btn).offsetTop - 120

            if(btn == 'projects') scrollTarget += 90
            if(btn == 'knowledge') scrollTarget -= 30
            // if(btn == 'about') scrollTarget += 20

            if(scrollTarget > scrollY) this.scrolling = 'D'
            else if(scrollTarget < scrollY) this.scrolling = 'U'
            else return

            const increaseScroll = 10

            const interval = setInterval(() => {
                if(scrollTarget == scrollY || !this.scrolling) {
                    clearInterval(interval)
                    this.scrolling = ''
                }

                if(this.scrolling == 'U'){
                    const total = scrollY - scrollTarget
                    if(total > increaseScroll) scrollY -= increaseScroll
                    else scrollY -= total
                    
                } else {
                    const total = scrollTarget - scrollY
                    if(total > increaseScroll) scrollY += increaseScroll
                    else scrollY += total
                }

                

                window.scrollTo(0, scrollY)
                
            }) 
        },

        viewMenu(){
            this.showMenu = !this.showMenu
        }
    }
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap');
:root{
    --blue: #3498db;
    --blue-hovered: #2e84bd;
    --white-background: rgb(220,220,230);
}
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Ubuntu', sans-serif;
}
html, body {
  scroll-behavior: smooth;
}
.container{
    max-width: 1024px;
    margin: 0 auto;
    padding: 0 4%;
}
#app > section{
    padding: 80px 0;
}
#app section > .container > h1:first-of-type{
    font-size: 30px;
    margin-bottom: 24px;
}
header{
    background-color: rgb(35,35,45);
    padding: 32px 0;
    text-align: center;
    position: fixed;
    width: 100%;
    z-index: 100;


    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    button{
        background: none;
        outline: 0;
        border: 0;
        color: white;
        cursor: pointer;
        font-size: 16px;
        margin: 0 18px;
        font-weight: 500;
        transition: color .1s;
    }

    button:hover{
        color:var(--blue);
    }

    button:active{
        color:var(--blue-hovered);
    }

    #logo{
        font-size: 28px;
        font-weight: bold;
    }

    nav{
        h1{
            color: white;
            font-size: 32px;
            margin-right: 16px;
            display: none;
            cursor: pointer;
        }

        ul li{
            display: inline-block;
        }

        
    }

}

#start{
    background-color: rgb(25,25,35);
    min-height: 640px;
    padding-top: 224px;
    text-align: center;
    color: rgb(255,255,255);

    p{
        font-size: 24px;
    }

    h1{
        font-size: 64px;
        color: var(--blue);
        display: inline-block;

        span{
            color: white;
            margin-left: -12px;
            animation-name: type;
            animation-duration: 0.5s;
            animation-fill-mode:forwards;
            animation-iteration-count: infinite
        }
    }

    a{
        display: inline-block;
        border: 3px solid var(--blue);
        color: var(--blue);
        border-radius: 8px;
        padding: 12px 32px;
        margin-top: 56px;
        text-decoration: none;
        font-weight: bold;
        transition: background-color .3s;
    }

    a:hover{
        background-color: var(--blue);
        color: rgb(235,235,235);
    }

    h2{
        font-size: 48px;
        margin-top: 72px;
        opacity: 90%;
        animation-name: arrow;
        animation-duration: 1s;
        animation-iteration-count: infinite
    }
}

#projects{
    text-align: center;
    color: rgb(10,10,10);
    background-color: rgb(225,225,235);

    .container{
        max-width: 768px;
    }

    .project{
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-between;

        img{
            height: 200px;
            border-radius: 8px;
            filter: brightness(75%);
        }

        .text{
            display: flex;
            flex-direction: column;
            justify-content: center;

            h1{
                margin-bottom: 8px;
                font-size: 22px;
            }

            .links{
                margin-top: 16px;

                a{
                    display: inline-block;
                    border: 3px solid var(--blue);
                    color: var(--blue);
                    border-radius: 8px;
                    padding: 8px 24px;
                    margin: 0 16px;
                    text-decoration: none;
                    font-weight: bold;
                    transition: background-color .3s;
                }

                a:hover{
                    background-color: var(--blue);
                    color: rgb(235,235,235);
                }
            }
        }
    }

    .project:not(:last-child){
        margin-bottom: 64px;
    }

    .project.rev{
        flex-direction: row;
    }

    a#more{
        color: var(--blue);
        text-decoration: none;
        font-size: 20px;
        font-weight: 500;
    }

    a#more:hover{
        color: var(--blue-hovered);
        text-decoration: underline;
    }
}

#knowledge{
    background-color: rgb(25,25,35);
    color: white;
    text-align: center;

    .icon{
        text-align: center;
        width: 128px;
        border-radius: 8px;
        display: inline-block;
        background-color: rgb(220,220,230);
        color: rgb(20,20,30);
        font-weight: bold;
        padding: 4px 0;
        margin-right: 16px;
        margin-bottom: 16px;
    }
}

#about{
    text-align: center;
    color: rgb(10,10,10);
    background-color: rgb(225,225,235);

    .container{
        max-width: 768px;
    }

    p{
        margin-bottom: 24px;
        margin-top: -8px;
    }
    
}

#contact{
    background-color: rgb(25,25,35);
    color: white;
    text-align: center;
    padding-bottom: 64px !important;

    a{
        color: white;
        font-size: 40px;
        margin: 0 16px;
        transition: color 0.3s;
    }

    a:hover{
        color: var(--blue);
    }

    a:active{
        color: var(--blue-hovered);
    }
}

footer{
    background-color: rgb(25,25,35);
    color: white;
    text-align: center;
    padding-bottom: 48px;

    button{
        background: none;
        color: white;
        font-size: 18px;
        border: 0;
        margin-bottom: 8px;
        outline: 0;
        cursor: pointer;
        font-weight: 500;
        transition: color .1s;
    }

    button:hover{
        color:var(--blue);
    }

    button:active{
        color:var(--blue-hovered);
    }

    hr{
        border: 1px solid rgba(200,200,200, 0.5);
        margin-bottom: 16px;
    }
}

@keyframes arrow {
    0%{ margin-top: 72px; }
    50%{ margin-top: 80px; }
    100%{ margin-top: 72px; }
}
@keyframes type {
    0%{ opacity: 1; }
    50%{ opacity: 0; }
}

@media screen and (max-width: 768px) {
    header{
        #logo{
            font-size: 32px;
        }
        nav{
            h1{
                display: block;
            }

            ul{
                display: none;
            }

            .show{
                display: block;
                position: fixed;
                left: 0;
                top: 96px;
                width: 100%;
                background-color: rgb(35,35,45);
                padding-bottom: 16px;

                li{
                    display: block;
                    margin: 16px 0;
                    
                    button{
                        font-size: 20px;
                    }
                }
            }
        }
    }

    #start h1{
        user-select: none;
    }

    #projects .project{
        flex-direction: column !important;

        .text{
            margin-top: 16px;
        }
    }
}
</style>
