<template>
    <aside>
        <div class="profile">
            <img src="../assets/profile.jpg" alt="">
            <p>Rodrigo Vitor</p>
        </div>
        <div class="links">
            <ul>
                <li><a href="#">Inicio</a></li>
                <li><a href="#sobre">Sobre mim</a></li>
                <li><a href="#resumo">Resumo</a></li>
                <li><a href="#servicos">Serviço</a></li>
                <li><a href="#porfolio">Porfolio</a></li>
                <li><a href="#skill">Habilidades</a></li>
                <li><a href="#contact">Contato</a></li>
            </ul>
        </div>
        <div class="footer-icons">
            <a href="https://www.linkedin.com/in/rodrigo-vitor-dev/" target="_blank" class="footer-icons-linkedin"><ion-icon name="logo-linkedin"></ion-icon></a>
            <a href="https://github.com/RodrigoVitor" target="_blank" class="footer-icons-github"><ion-icon name="logo-github"></ion-icon></a>
        </div>
    </aside>
</template>

<script>
export default {
    name: 'Aside-Vue'
}
</script>

<style scoped>
aside {
    width: 250px;
    min-height: 100vh;
    background-color: #111418;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    position: fixed;

}
aside div.profile {
    margin-top: 30px;
    text-align: center;
}
aside div img {
    width: 150px;
    border-radius: 100%;
    border: 6px solid #343A40
}
aside div p {
    color:white;
    font-size: 21px;
}

/* links */
ul li a {
    text-decoration: none;
    color: #fff;
    font-size: 16px;
}
li {
    list-style: none;
    text-align:center;
    line-height: 60px;
}
ul li a:hover {
    color: #BF2D11;
}

/* footer */
.footer-icons {
    text-align: center;
    padding-bottom: 10px;
}
.footer-icons ion-icon {
    color: #AAB1B8;
    font-size: 20px;
    margin-right: 22px;
}
.footer-icons-linkedin ion-icon:hover {
    color: #007bff
}
.footer-icons-github ion-icon:hover {
    color: #4d555a
}

@media screen and (max-width: 830px) {
    aside {
       display: none;
    }
}
</style>