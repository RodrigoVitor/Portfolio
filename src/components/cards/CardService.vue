<template>
    <div id="cardService">
        <span><ion-icon name="tv-outline"></ion-icon></span>
        <p>{{ title }}</p>
        <a href="#servicos" @click="openModal()">veja mais <ion-icon name="arrow-forward-outline"></ion-icon></a>
    </div>
</template>

<script>
export default {
    name: 'CardService',
    props: ['title', 'icon'],
    methods: {
        openModal() {
            this.$emit('openModal')
        }
    }
}
</script>

<style scoped>
#cardService {
    background-color: #343A40;
    width: 300px;
    margin: auto;
    padding: 40px 20px;
    text-align: center;
    position: relative;
}
#cardService span ion-icon {
    font-size:50px;
    color: #fff;
    margin-bottom: 10px;

}
#cardService p {
    font-size: 24px;
    color:#fff;
    margin-bottom: 10px;
}
#cardService a {
    color: #fff;
    display: flex;
    align-items: center;
    width: fit-content;
    padding: 5px;
    margin: auto;
    font-weight: bold;

}
#cardService a:hover {
    color: #DC3545
}
#cardService a:hover ion-icon {
    margin-left:10px;
    transition: margin-left 1s ease;
}
</style>