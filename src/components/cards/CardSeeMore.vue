<template>
    <div class="cardMain">
        <div class="cardSeeMore">
        <span @click="closeModal()"><ion-icon name="close-outline"></ion-icon></span>
        <div>
            <p class="title">{{ title }}</p>
            <p class="icon-text" v-for="task in tasks" v-bind:key="task"><ion-icon name="chevron-down-circle-outline"></ion-icon> {{ task }}</p>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'CardSeeMore',
    props: ['title', 'tasks'],
    methods: {
        closeModal() {
            this.$emit('closeModal')
        }
    }
}
</script>

<style>
.cardMain {
    background-color: rgba(0,0,0,.9);
    width: 100vw;
    height: 100vh;
    position: fixed;
    left: 0;
    top: 0;
}
.cardSeeMore {
    background-color: #343A40 ;
    width: 500px;
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
.cardSeeMore span {
    float: right;
    cursor: pointer;
}
.cardSeeMore span ion-icon {
    font-size: 40px;

}
.cardSeeMore div {
    float: left;
}
.cardSeeMore .title {
    font-size: 26px;
    margin-bottom: 20px;
}
.cardSeeMore div .icon-text {
    line-height: 35px;
    color: #C4BABA;
    text-align: justify;
}

@media screen and (max-width: 830px) {
    .cardSeeMore {
        width: 90%;
    }
}
</style>