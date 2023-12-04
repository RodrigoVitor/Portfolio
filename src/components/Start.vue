<template>
    <div id="bg-image">
        <p>Bem vindo</p>
        <h1 class="typing-text">Programador Web <span>Júnior</span></h1>
        <a class="btn" href="#contact">contato</a>

        <a href="#sobre" class="arrow"><ion-icon name="arrow-down-outline"></ion-icon></a>
    </div>
</template>

<script>
export default {
    name: "Start-Vue"
}
</script>

<style scoped>
div {
    background-image: url('../assets/bg-image.png');
    height: 100vh;
    background-repeat: no-repeat;
    background-size: cover;
    margin: 0 0 0 250px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
div p {
    font-size: 28px;
    color: #fff;
    font-weight: 500px;
}
div h1 {
    font-size: calc(1.525rem + 3.3vw);
    color: #fff;
    margin: 30px 0;
}
div a.btn {
    color: #f0340bc7;
    border:2px solid #f0340bc7;
    padding: 0.8rem 2.6rem;
    transition: all 0.5s ease;
    font-weight: 600;
    border-radius: 20px;
}
div a.btn:hover {
    color: #fff;
    background-color: #f0340bc7;
}

@media screen and (max-width: 830px) {
    div {
       margin:0
    }
    .typing-text span {
      display:none
    }
}

@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}   
.typing-text {
  overflow: hidden;
  white-space: nowrap;
  animation: typing 3s steps(20) infinite alternate;
  border-right: 4px solid #fff; /* Simula o cursor piscando */
}
.arrow {
  display: inline-block;
  font-size: 24px;
  animation: bounceArrow 2s ease-out infinite;
  font-size: 40px;
  color: #fff;
  position: absolute;
  bottom: 10px;
}

@keyframes bounceArrow {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(-20);
    opacity: 1;
  }
  40% {
    transform: translateY(0px);
    opacity: 0;
  }
  50% {
    transform: translateY(-30px);
    opacity: 1;
  }
}
</style>