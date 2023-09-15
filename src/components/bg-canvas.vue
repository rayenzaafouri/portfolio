<template>
  <div class="bg-partic"></div>
</template>
  
  <style scoped>
</style>
  
  <script>
class Particle {
  constructor(x, y, color, shape) {
    this.x = x;
    this.y = y;
    this.color = color;
    this.shape = shape;
  }
  data() {
    return { x: this.x, y: this.y, color: this.color, shape: this };
  }
}

export default {
  data() {
    return {

      //mblue
      circle_mblue: require("@/assets/particles/mblue/wave.png"),
      amiba_mblue: require("@/assets/particles/mblue/amiba.png"),
      demi_circle_mblue: require("@/assets/particles/mblue/demi-circle.png"),
      dot_mblue: require("@/assets/particles/mblue/dot.png"),
      rectangle_mblue: require("@/assets/particles/mblue/rectangle.png"),

      //blue
      circle_blue: require("@/assets/particles/blue/wave.png"),
      amiba_blue: require("@/assets/particles/blue/amiba.png"),
      demi_circle_blue: require("@/assets/particles/blue/demi-circle.png"),
      dot_blue: require("@/assets/particles/blue/dot.png"),
      rectangle_blue: require("@/assets/particles/blue/rectangle.png"),
      //fehling
      circle_fehling: require("@/assets/particles/fehling/wave.png"),
      amiba_fehling: require("@/assets/particles/fehling/amiba.png"),
      demi_circle_fehling: require("@/assets/particles/fehling/demi-circle.png"),
      dot_fehling: require("@/assets/particles/fehling/dot.png"),
      rectangle_fehling: require("@/assets/particles/fehling/rectangle.png"),

      //
      circle_purple: require("@/assets/particles/purple/wave.png"),
      amiba_purple: require("@/assets/particles/purple/amiba.png"),
      demi_circle_purple: require("@/assets/particles/purple/demi-circle.png"),
      dot_purple: require("@/assets/particles/purple/dot.png"),
      rectangle_purple: require("@/assets/particles/purple/rectangle.png"),

      //
      circle_yellow: require("@/assets/particles/yellow/wave.png"),
      amiba_yellow: require("@/assets/particles/yellow/amiba.png"),
      demi_circle_yellow: require("@/assets/particles/yellow/demi-circle.png"),
      dot_yellow: require("@/assets/particles/yellow/dot.png"),
      rectangle_yellow: require("@/assets/particles/yellow/rectangle.png"),
      shapes: [],
      density: 10,
      particlesArray: [],
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.shapes = [
  this.circle_mblue,
  this.amiba_mblue,
  this.demi_circle_mblue,
  this.dot_mblue,
  this.rectangle_mblue,
  
  this.circle_blue,
  this.amiba_blue,
  this.demi_circle_blue,
  this.dot_blue,
  this.rectangle_blue,

  this.circle_fehling,
  this.amiba_fehling,
  this.demi_circle_fehling,
  this.dot_fehling,
  this.rectangle_fehling,

  this.circle_purple,
  this.amiba_purple,
  this.demi_circle_purple,
  this.dot_purple,
  this.rectangle_purple,

        this.circle_yellow,
      this.amiba_yellow,
      this.demi_circle_yellow,
      this.dot_yellow,
     this. rectangle_yellow,
];

      const particlesCanvas = document.querySelector(".bg-partic");
      particlesCanvas.style.setProperty("width", "100%");
      particlesCanvas.style.setProperty("height", "100%");
      particlesCanvas.style.setProperty("top", "0");
      particlesCanvas.style.setProperty("left", "0");
      particlesCanvas.style.setProperty("z-index", "-1");
      particlesCanvas.style.setProperty("position", "absolute");

      const getRandomShape = () => {
        return this.shapes[parseInt(Math.random() * this.shapes.length)];
      };

      const getRandomColor = () => {
        let colors = ["#70DAC2", "#E979AB", "#37AAF9", "#F6B436", "#242021"];
        return colors[parseInt(Math.random() * colors.length)+ colors.length];
      };

      const getRandomCords = (x, y, gridCols, gridRows) => {
        const stepX = window.innerWidth / gridCols + 120;
        const stepY = window.innerHeight / gridRows + 120;
        const randomX = Math.random() * (x * stepX + 150) + x * stepX;
        const randomY = Math.random() * (x * stepY + 150) + y * stepY;
        return { x: randomX, y: randomY };
      };

      const drawParticle = (particle) => {
        let element = document.createElement("img");
        element.classList.add("particle");
        element.src = getRandomShape();
        //element.style.setProperty("background-color", particle.color);
        element.style.setProperty("position", "fixed");

        particlesCanvas.appendChild(element);
        element.style.setProperty("top", particle.x + "px");
        element.style.setProperty("left", particle.y + "px");
        element.style.setProperty("animation", "fadeIn 5s");
        return;
      };




      const gridX = 15;
      const gridY = 6;

      for (let i = 0; i <= gridX; i++) {
        for (let j = 0; j <= gridY; j++) {
          let cords = getRandomCords(i, j, gridX, gridY);
          let particle = new Particle(
            cords.x,
            cords.y,
            getRandomColor(),
            getRandomShape()
          );
          this.particlesArray.push(particle);
          drawParticle(particle);
        }
      }
    });
  },
};
</script>
  
  <style>

  .bg-partic{
    filter: blur(2.5px);
    overflow: hidden;
    height: 250dvh;
    
  }
</style>
  