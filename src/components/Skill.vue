<template>
    <div id="skill">
        <h2>Conhecimentos</h2>
        <div class="grid">
            <div class="front">
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">HTML5</span>
                        <span style="color: #fff">90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 90%;"></div>
                    </div>
                </div>
        
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">CSS3</span>
                        <span style="color: #fff">85%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 85%;"></div>
                    </div>
                </div>
        
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Javascript</span>
                        <span style="color: #fff">67%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 67%;"></div>
                    </div>
                </div>
        
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Vue</span>
                        <span style="color: #fff">35%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 35%;"></div>
                    </div>
                </div>
        
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Typescript</span>
                        <span style="color: #fff">10%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 10%;"></div>
                    </div>
                </div>
            </div>
    
            <div class="other">
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">PHP</span>
                        <span style="color: #fff">65%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 65%;"></div>
                    </div>
                </div>
    
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Laravel</span>
                        <span style="color: #fff">39%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 39%;"></div>
                    </div>
                </div>
    
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">MySql</span>
                        <span style="color: #fff">30%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 30%;"></div>
                    </div>
                </div>
    
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Git</span>
                        <span style="color: #fff">70%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 70%;"></div>
                    </div>
                </div>
    
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Figma</span>
                        <span style="color: #fff">35%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 25%;"></div>
                    </div>
                </div>
    
                <div class="progress-container">
                    <div class="progress-name">
                        <span style="color: #F0340B">Gimp</span>
                        <span style="color: #fff">40%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 40%;"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillVue'
}
</script>

<style scoped>
#skill {
    margin: 0 0 0 250px;
    background-color: #212529;
    padding: 80px 0;
}
#skill h2 {
    text-align: center;
    color: #fff;
    font-size: 36px;
}
.progress-container {
  width: 100%;
  text-align: center;
}
.progress-name {
  margin-bottom: 10px;
  display:flex;
  justify-content: space-between;
}
.progress-bar {
  width: 100%;
  height: 10px;
  background-color: #e0e0e0;
  border-radius: 5px;
  overflow: hidden;
}
.progress-fill {
  height: 100%;
  background-color: #EE5D3D;
  border-radius: 5px;
  transition: width 0.5s ease-in-out;
}
.grid {
    display:grid;
    grid-template-columns: 400px 400px;
    justify-content: center;
    gap: 50px;
}



@media screen and (max-width: 830px) {
    div#skill {
       margin:0
    }
    .grid {
        grid-template-columns: 80%;
    }
}
</style>