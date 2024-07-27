<template>
    <div id="resumo">
        <h2>Minhas experiências</h2>
        <div class="card">
            <p class="date">Fev/2024 - Atual</p>
            <img src="../assets/hc.png" alt="hotel crisal" width="400px"> <br>
            <span>Recepcionista</span>
            <p class="info">
                Responsável pelo agendamento de reservas por e-mail, WhatsApp e telefone, pela emissão de notas fiscais e pela criação e manutenção de planilhas no Excel.
            </p>
            <p class="stacks"><span>Stacks:</span> Comunicação, Excel Básico </p>
        </div>
        <div class="card">
            <p class="date">Jun/2023 - Nov/2023</p>
            <img src="../assets/ig.png" alt=""> <br>
            <span>Desenvolvedor de back end</span>
            <p class="info">
                    Desenvolvimento, programação, codificando e revisando códigos;
                            Melhorias de performance de fluxos existentes;
                        Alteração de códigos, consultas e atualizações no banco;
                    Resolução de bugs/e ou problemas.
            </p>
            <p class="stacks"><span>Stacks:</span> PHP · Laravel · PhpMyAdmin · Back-end </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ResumeVue'
}
</script>

<style scoped>
div#resumo {
    margin: 0 0 0 250px;
    background-color: #343A40;
    padding: 80px 0 10px 0;
}
div h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
div.card {
    width: 450px;
    margin: 40px auto;
    border: 1px solid #212529;
    padding: 22px;
}
div.card p.date {
    background-color: #C23112;
    width: fit-content;
    padding: 2px 10px;
    border-radius:16px;
    color:#fff;
    font-size: 14px;
    margin-bottom: 10px;
}
div.card > span {
    color: #C63617;
    font-weight: bold;
    font-size: 16px;
}
div.card p.info, p.stacks {
    margin-top: 20px;
    color:#fff;
}
p.stacks span {
    font-weight: bold;
}
@media screen and (max-width: 830px) {
    div#resumo {
       margin:0
    }
    div.card {
        width: auto;
    }
}
</style>