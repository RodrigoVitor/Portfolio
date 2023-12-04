<template>
    <div id="contact">
        <h2>Fale comigo</h2>
        <div class="contact-data">
            <p class="contact-data-title">ENDEREÇO</p>
            <p class="contact-data-res"><ion-icon name="home-outline"></ion-icon> Santa Rita do Sapucaí / MG</p>
            <p class="contact-data-res"> <ion-icon name="call-outline"></ion-icon> (35) 997401598</p>
            <p class="contact-data-res"><ion-icon name="home-outline"></ion-icon>rodrigovitor400@gmail.com</p>
        </div>
    </div>
</template>


<script>
export default {
    name: 'ContactMe'
}
</script>

<style scoped>
div#contact {
    margin: 0 0 0 250px;
    background-color: #343A40;
    padding: 80px 0 40px 40px;
}
div h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
.contact-data {
    color: #fff;
}
.contact-data-title {
    font-size:21px;
    margin: 40px 0 20px 0;
}
.contact-data-res {
    display: flex;
    gap: 10px;
    margin: 10px 0;
}
.contact-data-res ion-icon {
    color: #fff;
    font-size:22px;
}


@media screen and (max-width: 830px) {
    div#contact {
       margin:0
    }
}
</style>

