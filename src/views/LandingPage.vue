
<template>
  <darkmodeSwitcher/>
  <bg-canvas/>
  <dev-intro/>
  <dev-buttons/>

</template>


<script>
import DevIntro from '@/components/dev-intro.vue';
//import navbarTranslucid from '@/components/navbar-translucid.vue';
import bgCanvas from '@/components/bg-canvas.vue';
import devButtons from '@/components/dev-buttons.vue';
import darkmodeSwitcher from '@/components/darkmode-switcher.vue';
  
export default {
  components: {
    DevIntro,bgCanvas,devButtons,darkmodeSwitcher
  }
}

</script>
<style scoped>
</style>