<template>
    <header>
        <nav>
            <p>Rodrigo Vitor</p>
            <div>
                <a href="https://www.linkedin.com/in/rodrigo-vitor-9a7354268/" target="_blank"><ion-icon name="logo-linkedin"></ion-icon></a>
                <a href="https://github.com/Rodrigo-Vitor" target="_blank"><ion-icon name="logo-github"></ion-icon></a>
                <a href="#" @click="openCloseMenu()"><ion-icon name="menu-outline"></ion-icon></a>
                <ul id="menu-icon">
                    <li><a href="#">Inicio</a></li>
                    <li><a href="#sobre">Sobre mim</a></li>
                    <li><a href="#resumo">Resumo</a></li>
                    <li><a href="#servicos">Serviço</a></li>
                    <li><a href="#porfolio">Porfolio</a></li>
                    <li><a href="#skill">Habilidades</a></li>
                    <li><a href="#contact">Contato</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>
  
  <script>
  export default {
    name: 'NavBar',
    data: function () {
        return {
            isMenu: false,
            innerWidth: window.innerWidth
        }
    },
    methods: {
        openCloseMenu () {
            this.isMenu = !this.isMenu
            if(this.isMenu) {
                document.getElementById('menu-icon').style.top = '50px'
            } else {
                document.getElementById('menu-icon').style.top = '-900px'
            }
        },
        handleResize () {
            this.windowWidth = window.innerWidth;
        }
    },
    mounted() {
     window.addEventListener('resize', this.handleResize);
    },
    beforeUnmount() {
        window.removeEventListener('resize', this.handleResize);
    }
  }
  </script>

<style scoped>
    header {
        display:none;
    }

  @media  screen and (max-width: 830px) {
      header {
          background-color: #111418;
          position: relative;
          width: 100vw;
          display: block;
          padding: 10px;
      }
      header nav {
          display: flex;
          align-items: center;
          justify-content: space-around;
      }
      header nav p {
          color:white;
          font-size: 24px;
      }
      header ion-icon {
          color: #AAB1B8;
          font-size: 20px;
          margin-right: 22px;
      }
      header nav div ul {
          position: absolute;
          background-color: rgba(3,2,1, 0.9);
          left: 0;
          top:-900px;
          width: 100vw;
          padding: 0;
          transition: top 2s ease;
      }
      header nav div ul li {
          list-style: none;
          border-bottom: 1px solid #ccc;
          padding: 20px;
      }
      header nav div ul li a {
          text-decoration: none;
          color: #fff;
          font-size: 24px; 
      }
      header nav div ul li a:hover {
          color: #BF2D0E
      }
  }
</style>
  