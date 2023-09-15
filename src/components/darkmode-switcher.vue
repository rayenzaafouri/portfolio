<template>
  <div @click="toggleDarkMode"> <i class="fa-solid fa-moon"></i><span>Enable dark mode</span></div>
  
</template>
  
  <style scoped>
  div{
    color: black;
    font-size: .75em;
    right: .5em;
    top: .5em;
    position: fixed;
    z-index: 5;
    cursor: pointer;
    background: #2c3e50;
    border-radius:16px;
    background: rgba(191, 179, 179, 0.2);
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 30px;
    -webkit-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(191, 179, 179, 0.28);
    padding: .5em;
    

  }
  div > * {
        cursor: pointer;

    margin: 0 .5em  ;
  }
</style>
  
  <script>
export default{
  data() {
    return { isDarkMode : false };
  },
  methods : {
    toggleDarkMode : function(){
      //Custom:
      document.body.style.setProperty("background-color","black")
      const hero = document.querySelectorAll(".dev-intro > h2")
      hero.forEach(element =>{
        element.style.color = "#2980b9"
      })

      document.querySelector(".dev-buttons").style.setProperty  ("filter","brightness(0.75)")


      //Text based
      const elts = [".overview-p",".dev-buttons"]
      if(!this.isDarkMode){
        for(let i in elts){
          document.querySelector(elts[i]).style.setProperty("color","white")

          
        }
        
      }
    }
  }
}
</script>