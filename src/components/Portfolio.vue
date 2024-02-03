<template>
    <div id="porfolio">
        <h2>Portfolio</h2>
        <div class="links">
            <span @click="changeLink('todos')" :class="link == 'todos' ? 'active' : ''">Todos</span>
            <span @click="changeLink('front')" :class="link == 'front' ? 'active' : ''">Front-end</span>
            <span @click="changeLink('back')" :class="link == 'back' ? 'active' : ''">Back-end</span>
            <span @click="changeLink('figma')" :class="link == 'figma' ? 'active figma-link' : ''">Design Figma</span>
        </div>
        <div class="links-todos" v-if="link == 'todos'">
            <span @click="openModal('Portfolio', 'Este é o meu portfólio, criado com o objetivo de destacar e compartilhar minha experiência, demonstrando meu conjunto de habilidades e proporcionando uma breve visão sobre quem eu sou.', ['HTML, ', 'CSS, ', 'VUE'], 'Dez 03, 2023', 'portfolio', true, 'https://github.com/RodrigoVitor/portfolio', 'https://rodrigodev.netlify.app/', null)">
                <div class="links-todos-card">
                    <img src="../assets/portfolio.png" alt="Portfolio">
                    <div>
                        <p>Portfolio <span>Front end</span></p>
                    </div>
                </div>
            </span>
            <span @click="openModal('Gerenciador de notas', 'Aplicativo de gerenciamento de notas onde os usuários podem se cadastrar, fazer login e criar, editar e excluir suas notas. As notas podem ser organizadas por categorias, permitindo que os usuários mantenham suas informações organizadas e acessíveis.', ['HTML, ', 'CSS, ', 'PHP, ', 'LARAVEL, ', 'MySql'], 'Nov 30, 2023', 'notes', true, 'https://github.com/RodrigoVitor/Gerenciador-de-notas', null, null)">
                <div class="links-todos-card">
                    <img src="../assets/notes.png" alt="Portfolio">
                    <div>
                        <p>Gerenciador de notas <span>Back end</span></p>
                    </div>
                </div>
            </span>
            <span @click="openModal('Emprego Srs', 'Plataforma de empregos para moradores de Santa Rita do Sapucai, MG', ['Figma'], '24/01/2024', 'empregosrs', true, 'https://www.figma.com/file/Q5EwmbYcKxbVFrB2xuVWkN/Emprego-Srs?type=design&node-id=0%3A1&mode=design&t=4EaBNn9MhIN0Yh1a-1', null, 'https://www.figma.com/file/Q5EwmbYcKxbVFrB2xuVWkN/Emprego-Srs?type=design&node-id=0%3A1&mode=design&t=4EaBNn9MhIN0Yh1a-1')">
                <div class="links-todos-card">
                    <img src="../assets/empregosrs.png" alt="Portfolio">
                    <div>
                        <p>Emprego Srs <span>Figma</span></p>
                    </div>
                </div>
            </span>
            <span>
                <div class="links-todos-card developing">
                    <img src="../assets/empregosrs-back.png" alt="Portfolio">
                    <div>
                        <p style="cursor: default;">Emprego Srs - Em desenvolvimento <span style="cursor: default;">Back end</span></p>
                    </div>
                </div>
            </span>
            <!-- <span @click="openModal('Vagas Devs', 'Plataforma web projetada para simplificar a busca e candidatura a oportunidades de emprego para programadores.', ['HTML, ', 'CSS, ', 'PHP, ', 'LARAVEL, ', 'MySql'], 'Nov 30, 2023', 'vagas', false, 'https://github.com/Rodrigo-Vitor/Vagas-Devs', null)">
                <div class="links-todos-card">
                    <img src="../assets/vagas-dev.png" alt="Portfolio">
                    <div>
                        <p>Vagas Devs <span>Back end</span></p>
                    </div>
                </div>
            </span> -->
        </div>
        <div class="links-todos" v-if="link == 'front'">
            <span @click="openModal('Portfolio', 'Este é o meu portfólio, criado com o objetivo de destacar e compartilhar minha experiência, demonstrando meu conjunto de habilidades e proporcionando uma breve visão sobre quem eu sou.', ['HTML, ', 'CSS, ', 'VUE'], 'Dez 03, 2023', 'portfolio', true, 'https://github.com/RodrigoVitor/portfolio', 'https://rodrigodev.netlify.app/', null)">
                <div class="links-todos-card">
                    <img src="../assets/portfolio.png" alt="Portfolio">
                    <div>
                        <p>Portfolio <span>Front end</span></p>
                    </div>
                </div>
            </span>
        </div>
        <div class="links-todos" v-if="link == 'back'">
            <span @click="openModal('Gerenciador de notas', 'Aplicativo de gerenciamento de notas onde os usuários podem se cadastrar, fazer login e criar, editar e excluir suas notas. As notas podem ser organizadas por categorias, permitindo que os usuários mantenham suas informações organizadas e acessíveis.', ['HTML, ', 'CSS, ', 'PHP, ', 'LARAVEL, ', 'MySql'], 'Nov 30, 2023', 'notes', true, 'https://github.com/RodrigoVitor/Gerenciador-de-notas', null, null)">
                <div class="links-todos-card">
                    <img src="../assets/notes.png" alt="Portfolio">
                    <div>
                        <p>Gerenciador de notas <span>Back end</span></p>
                    </div>
                </div>
            </span>
            <span>
                <div class="links-todos-card developing">
                    <img src="../assets/empregosrs-back.png" alt="Portfolio">
                    <div>
                        <p style="cursor: default;">Emprego Srs - Em desenvolvimento <span style="cursor: default;">Back end</span></p>
                    </div>
                </div>
            </span>
        </div>
        <div class="links-todos" v-if="link == 'figma'">
            <span @click="openModal('Emprego Srs', 'Plataforma de empregos para moradores de Santa Rita do Sapucai, MG', ['Figma'], '24/01/2024', 'empregosrs', true, 'https://www.figma.com/file/Q5EwmbYcKxbVFrB2xuVWkN/Emprego-Srs?type=design&node-id=0%3A1&mode=design&t=4EaBNn9MhIN0Yh1a-1', null, 'https://www.figma.com/file/Q5EwmbYcKxbVFrB2xuVWkN/Emprego-Srs?type=design&node-id=0%3A1&mode=design&t=4EaBNn9MhIN0Yh1a-1')">
                <div class="links-todos-card">
                    <img src="../assets/empregosrs.png" alt="Portfolio">
                    <div>
                        <p>Emprego Srs <span>Figma</span></p>
                    </div>
                </div>
            </span>
        </div>
        <CardPortfolio 
            :title="title" :info="info" :tecs="tecs" :data="data" :src="src" :finish="finish" :github="github" :site="website" :figma="figma"
            @closeModal="closeModal()" 
            v-if="isModal"
        />
    </div>
</template>

<script>
import CardPortfolio from './cards/CardPortfolio.vue'
export default {
    name: 'PorfolioVue',
    components: {
        CardPortfolio
    },
    data () {
        return {
            link: 'todos',
            isModal: false,
            title: '',
            info: '',
            tecs: '',
            data: '',
            src: '',
            finish: '',
            github: '',
            website: '',
            figma: null
        }
    },
    methods: {
        changeLink (value) {
            this.link = value
        },
        closeModal () {
            this.isModal = false
        },
        openModal (title, info, tecs, data, src, finish, github, website, figma) {
            this.title = title
            this.info = info
            this.tecs = tecs
            this.data = data
            this.src = src
            this.finish = finish
            this.isModal = true
            this.github = github
            this.website = website,
            this.figma = figma
        }
    }
}
</script>

<style scoped>
div#porfolio {
    margin: 0 0 0 250px;
    background-color: #343A40;
    padding: 80px 0 40px 0;
}
div h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
.links {
    text-align: center;
    font-size: 16px;
    margin: 40px 0;
}
.links span {
    margin-right: 24px;
    cursor: pointer;
    color:#9A9DA0
}
.links span:hover {
    color:#F0340B
}
.links span.active {
    color: #F0340B;
    border-bottom: 2px solid #F0340B;
    padding-bottom: 10px;
}
.links-todos {
    display:grid;
    grid-template-columns: auto auto;
    align-items: center;
    justify-content: center;
    gap: 40px;
}
.links-todos span {
    cursor: pointer;
}
.links-todos-card {
    position: relative;
    display: flex;
}
.developing {
    cursor:default
}
.links-todos-card img {
    width: 350px;
    height: 160px;
}
.links-todos-card p span {
    color: #ccc;
    font-weight: 700;
}
.links-todos-card div {
    color:#fff;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0,0,0, 0.9);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    visibility: hidden ;
    opacity: 0;
}
.links-todos span:hover .links-todos-card div {
    visibility: visible;
    opacity: 1;
    transition: visibility 0s, opacity 0.5s
}
.links-todos-card div p span {
    display: block;
    transition: visibility 0s, opacity 0.5s;
}

@media screen and (max-width: 830px) {
    div#porfolio {
       margin:0
    }
    .links {
        display: grid;
        grid-template-columns: auto auto;
    }
    .links span {
        margin-top: 30px;
    }
    .links-todos {
        grid-template-columns: auto;
    } 
}
</style>