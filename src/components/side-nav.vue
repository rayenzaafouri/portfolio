<template>
    <div class="sidenav-wrapper">
        <a href="#overview">overview</a>
        <a href="#skills">skills</a>
        <a href="#hireme">hire me</a>
    </div>
    
    <div class="sidenav-scroller"></div>
</template>

<script>
export default {
  mounted: function () {
    this.$nextTick(function () {
      const sidenav = document.querySelector(".sidenav-wrapper")
      const scroller = document.querySelector(".sidenav-scroller")

      console.log({ sidenav, scroller })
      const sidenav_rect = sidenav.getBoundingClientRect()
      console.log({ sidenav_rect })

      scroller.style.setProperty('width', (sidenav_rect.width + 10) + "px")
      scroller.style.setProperty('height', sidenav_rect.height + "px")
      scroller.style.setProperty('left', sidenav_rect.left + "px")
      scroller.style.setProperty('top', sidenav_rect.top + "px")

      //click 1
      document.querySelector(".sidenav-wrapper>a:nth-of-type(1)").addEventListener("click", function () {
        const targetElement = document.querySelector('.dev-intro');
        targetElement.scrollIntoView({
          behavior: 'auto',
          block: 'start',
        });
      })

      //scroller sync

      const syncScroller = (a) => {
        const element = document.querySelector(a);
        if (element) {
          const element_props = element.getBoundingClientRect();
          scroller.style.setProperty('top', element_props.top + "px");
          scroller.style.setProperty('height', element_props.height + "px");
        }
      };
      // sidenav scrollspy observer 

      window.addEventListener('scroll', function () {
        const skills_delimiter = document.querySelector('.navbar-safe');
        const skills_rect = skills_delimiter.getBoundingClientRect();
        skills_delimiter.style.setProperty("opacity","0")


        if (skills_rect.top >= 0 && skills_rect.bottom  <= window.innerHeight) {
          syncScroller(".sidenav-wrapper > a:nth-of-type(2)");
          document.querySelector('.d-palette').style.setProperty("animation","cardReveal 1.5s forwards")

        }

        const dev_intro_delimiter = document.querySelector('.dev-intro');
        const dev_intro_rect = dev_intro_delimiter.getBoundingClientRect();

        if (dev_intro_rect.top >= 0 && dev_intro_rect.bottom<= window.innerHeight) {
          syncScroller(".sidenav-wrapper > a:nth-of-type(1)");
          
          
        }


        const hireme_delimiter = document.querySelector('.hire-me');
        hireme_delimiter.style.setProperty("opacity","0")
        document.querySelectorAll(".hire-me")[1].style.setProperty("opacity","0")
        const hireme_rect = hireme_delimiter.getBoundingClientRect();

        if (hireme_rect.top >= 0 && hireme_rect.bottom  <= window.innerHeight) {
          syncScroller(".sidenav-wrapper > a:nth-of-type(3)");

          hireme_delimiter.style.setProperty("animation","cardReveal 1.5s forwards")
          document.querySelectorAll(".hire-me")[1].style.setProperty("animation","cardReveal 1.5s forwards")
          
        }
      });
    })
  }
}
</script>

<style scoped>
.sidenav-wrapper {
    position: fixed;
    top: 45dvh;
    display: flex;
    flex-direction: row-reverse;
    transform: rotate(-90deg);
    gap: 15px;
    padding: 0;
}

.sidenav-scroller {
    position: fixed;
    display: flex;
    flex-direction: row-reverse;
    z-index: -1;
    transform: translateX(-3px);
    border-radius: 16px;
    padding: 20px 20px 0;
    transition: all .5s;
    background: rgba(191, 179, 179, 0.2);
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 30px;
    backdrop-filter: blur(5px);
    border: 1px solid rgba(191, 179, 179, 0.28);
}

a {
    all: unset;
    cursor: pointer;
    padding: .75em 0.5em;
    border-radius: 16px;
    text-align: center;
    text-transform: capitalize;
}
</style>
