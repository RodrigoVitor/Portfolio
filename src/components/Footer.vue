<template>
    <div id="footer">
        <p>Copyright © 2023 <a href="#">Rodrigo Vitor</a></p>
    </div>
</template>

<script>
export default {
    name: 'FooterVue'
}
</script>

<style scoped>
#footer {
    margin: 0 0 0 250px;
    background-color: #212529;
    padding: 80px 0 80px 40px;
}

#footer p {
    color: #fff;
}

#footer p a {
    color: #C23112
}

@media screen and (max-width: 830px) {
    div#footer {
       margin:0
    }
}
</style>