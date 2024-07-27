<template>
    <div id="sobre">
        <h2>Um pouco sobre mim</h2>
        <div class="box">
            <p class="text-about">Eu sou <span>Rodrigo Vitor</span>, um programador web júnior</p>
            <p class="text-desc">Olá pessoal! Meu nome é Rodrigo Vitor, e sou um apaixonado por tecnologia 🚀.</p> <br>
            <p class="text-desc">Atuei como desenvolvedor Back-end com PHP na empresa ImovelGuide, onde tive a oportunidade de colocar em prática o conhecimento adquirido e adquirir novas habilidades. Cada dia é uma oportunidade para aprender algo novo e enfrentar desafios em pequenos projetos.</p> <br>
            <p class="text-desc">Minas Gerais é meu lar, mas minha paixão pela programação e tecnologia transcende fronteiras.</p> <br>
            <p class="text-desc">Sempre fui um autodidata, acreditando que a disciplina e a dedicação são essenciais para o sucesso. Não vejo a programação como uma competição com os outros, mas como uma jornada de superação pessoal. Tenho uma grande paixão por ajudar os outros e entendo que esse caminho não é fácil. No entanto, mantenho-me firme e determinado na busca dos meus objetivos.</p> <br>
            <p class="text-desc">Estou entusiasmado com as possibilidades que a programação oferece e estou comprometido em continuar aprendendo e crescendo nesse campo. Tenho a convicção de que, com perseverança e esforço contínuo, poderei alcançar grandes conquistas</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutMe'
}
</script>

<style scoped>
div#sobre {
    margin: 0 0 0 250px;
    background-color: #212529;
    padding: 80px 0 10px 0;
}
div h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
div.box {
    width:70%;
    margin: 80px auto;
}
.text-about {
    font-size: 26px;
    color: #fff;
    font-weight: 600;
    margin-bottom: 26px;
}
.text-about span {
    color: #C23112
}
.text-desc {
    color:#8B8D8F;
    font-size: 16px;
    line-height: 33px;
}

@media screen and (max-width: 830px) {
    div#sobre {
       margin:0
    }
}
</style>