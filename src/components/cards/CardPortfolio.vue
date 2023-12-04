<template>
    <div class="cardMain">
        <div class="cardPortfolio">
        <span @click="closeModal()"><ion-icon name="close-outline"></ion-icon></span>
        <div>
            <p class="title">{{ title }}</p>
            <div class="content">
                <img v-if="src == 'portfolio'" src="../../assets/portfolio.png" width="400" alt="Portfolio">
                <img v-if="src == 'notes'" src="../../assets/notes.png" width="400" alt="Portfolio">
                <img v-if="src == 'vagas'" src="../../assets/vagas-dev.png" width="400" alt="Portfolio">
                <div class="content-info">
                    <p class="content-info-title">Informações do projeto:</p>
                    <span class="content-info-desc">{{ info }}</span>
                    <p class="content-info-title">Detalhes do projeto:</p>
                    <p class="content-info-tec"><span>Tecnologia:</span> <i v-for="tec in tecs" v-bind:key="tec">{{ tec }} </i></p>
                    <p class="content-info-data"><span>Data:</span> {{ data }}</p>
                    <p class="content-info-links"><span>Links: </span>
                        <a :href="github" target="_blank" class="src"><ion-icon name="logo-github"></ion-icon></a>
                        <a :href="site" target="_blank" class="world" v-show="site !== null"><ion-icon name="globe-outline"></ion-icon></a>
                    </p>
                    <p v-if="!finish" class="content-info-status">Em desenvolvimento </p>
                   
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'cardPortfolio',
    props: ['title', 'info', 'tecs', 'data', 'src','finish', 'github', 'site'],
    methods: {
        closeModal() {
            this.$emit('closeModal')
        }
    }
}
</script>

<style scoped>
.cardMain {
    background-color: rgba(0,0,0,.9);
    width: 100vw;
    height: 100vh;
    position: fixed;
    left: 0;
    top: 0;
}
.cardPortfolio {
    background-color: #fff/* #343A40 */ ;
    width: 70%;
    margin: auto;
    padding: 40px 20px;
    text-align: center;
    position: fixed;
    color: #fff;
    padding: 40px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    /* display: none; */
}
.cardPortfolio > span {
    float: right;
    cursor: pointer;
}
.cardPortfolio > span ion-icon {
    font-size: 40px;
    color: #252b33;
}
.cardPortfolio .title {
    font-size: 26px;
    margin-bottom: 20px;
    color: #252b33 ;
    font-weight: 600;
}
.content {
    display:grid;
    grid-template-columns: auto auto;
    gap: 20px;
    align-items: center;
}
.content div {
    text-align: left;
}

.content-info-title {
    font-weight: 600;
    color: #252b33;
    margin: 15px 0 5px 0;
}
.content-info-desc, .content-info-tec, .content-info-data, .content-info-links, .content-info-status {
    color:#4c4d4d;
    line-height: 28px;
}
.content-info-tec span, .content-info-data span, .content-info-links span {
    font-weight: 600;
}
.content-info-tec, .content-info-data {
    border-bottom: 1px solid #4c4d4d;
    padding-bottom: 10px;
    margin: 0 0 20px 0;
}
.content-info-links {
    display: flex;
    gap: 20px;
}
.content-info-links a ion-icon {
    font-size:26px;
    color: #252b33;
}
.content-info-links a ion-icon:hover {
    color: #4c4d4d
}

@media screen and (max-width: 830px) {

    .cardPortfolio {
        width: 95%;
        height: 400px;
        overflow: scroll;
    }
    .content {
        grid-template-columns: auto;
    }
    .content img {
        width: 90%;
    }
}
</style>