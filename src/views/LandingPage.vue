
<template>
  <darkmodeSwitcher/>
  <bg-canvas/>
  <dev-intro/>
  <dev-buttons/>
  <side-nav/>
  <contentWtitle/>
  <hireMe/>
</template>


<script>
import DevIntro from '@/components/dev-intro.vue';
//import navbarTranslucid from '@/components/navbar-translucid.vue';
import bgCanvas from '@/components/bg-canvas.vue';
import devButtons from '@/components/dev-buttons.vue';
import darkmodeSwitcher from '@/components/darkmode-switcher.vue';
import sideNav from '@/components/side-nav.vue'
import contentWtitle from '@/components/content-w-title'
import hireMe from '@/components/hire-me.vue'
  
export default {
  components: {
    DevIntro,bgCanvas,devButtons,darkmodeSwitcher,sideNav,contentWtitle,hireMe
  }
}

</script>
<style>

body::-webkit-scrollbar {
  width: 0.5rem; 
}
body::-webkit-scrollbar-thumb {
  background: rgba(191, 179, 179, 0.2);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(191, 179, 179, 0.28);
}
body {
  transition : background .7s;
    scrollbar-width: none; 
  -ms-overflow-style: none;
  padding-bottom:2em ;
}
a ,h2,p {
  transition: color .5s;
} 


</style>