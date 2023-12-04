<template>
    <div id="servicos">
        <h2>Serviços</h2>
        <div class="flex">
            <CardService
            @openModal="openModal('Web Design', ['Desenvolvo o layout da sua aplicação web.', 'Faço edição das imagens.', 'Crio logótipos de marcas', 'E muito mais...'])" 
                title="Web Design"
            />
            <CardService 
                @openModal="openModal('Front end', ['Crio landing pages', 'Desenvolvo páginas com designs variados', 'Manutenção de códigos', 'Crio a responsividade do seu site', 'Implementações de novas funcionalidades', 'E muito mais...'])" 
                title="Front end"
            />
            <CardService 
                @openModal="openModal('Back end', ['Desenvolvimento de APIs', 'Otimização de Consultas em Banco de Dados', 'Segurança e Autenticação', 'Manutenção e Atualização', 'E muito mais...'])"
                 title="Back end"
            />
            <CardSeeMore @closeModal="closeModal()" :title="title" :tasks="tasks" v-if="isOpenModal" />
        </div>
    </div>
</template>

<script>
import CardService from './cards/CardService'
import CardSeeMore from './cards/CardSeeMore'

export default {
    name: 'ServiceVue',
    components: {
        CardService,
        CardSeeMore
    },
    data () {
        return {
            isOpenModal:false,
        }
    },
    methods: {
        openModal(title, tasks) {
            this.title = title
            this.tasks = tasks
            this.isOpenModal = true
        },
        closeModal() {
            this.isOpenModal = false
        }
    }
}
</script>

<style scoped>
#servicos {
    margin: 0 0 0 250px;
    background-color: #212529;
    padding: 80px 0;
}
div#servicos h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
.flex {
    display:flex;
    margin-top: 40px;
}


@media screen and (max-width: 830px) {
    div#servicos {
       margin:0
    }
    .flex {
        flex-direction: column;
        gap: 20px;
    }
}
</style>