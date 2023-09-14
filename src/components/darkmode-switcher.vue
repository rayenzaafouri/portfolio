<template>
  <div @click="toggleDarkMode"> <i class="fa-solid fa-moon"></i><span>Enable dark mode</span></div>
  
</template>
  
  <style scoped>
  div{
    font-size: .75em;
    background:transparent;
    right: .5em;
    top: .5em;
    position: fixed;
    z-index: 5;
    cursor: pointer;
    background: #2c3e50;
    border-radius:16px;
    color: white;
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