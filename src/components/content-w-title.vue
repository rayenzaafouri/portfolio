<template>
<div class="navbar-safe" id="skills"></div>
<div class="d-palette" >
     <h3 class="title">My digital palette has the following technologies : </h3>
     <br>
    <h2>Backend</h2>
    <div class="tech-display">
        <img src="https://aety.io/wp-content/uploads/2016/11/mysql-logo.png" alt="">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/2560px-Node.js_logo.svg.png" alt="">
        <img src="https://res.cloudinary.com/practicaldev/image/fetch/s--RK-AgEnh--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/1s3bedypkt7zm8maikzg.png" alt="">
        <img src="https://logos-world.net/wp-content/uploads/2021/10/Python-Symbol.png" alt="">

    </div>
    <h2>Frontend</h2>
    <div class="tech-display">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/555px-Vue.js_Logo_2.svg.png" alt="Vue.js">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/HTML5_Badge.svg/1200px-HTML5_Badge.svg.png" alt="HTML5">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/CSS3_logo.svg/1200px-CSS3_logo.svg.png" alt="CSS3">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/JavaScript-logo.png/800px-JavaScript-logo.png" alt="Javascript">

    </div>


    <h2>Tooling</h2>
    <div class="tech-display">
        <img src="https://variwiki.com/images/archive/a/a1/20190926132947%21Docker.png" alt="">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1920px-Git-logo.svg.png">
        <img src="https://1000logos.net/wp-content/uploads/2017/03/Symbol-Linux.jpg">
        <img src="https://cdn-images-1.medium.com/max/1197/1*BFTWWQO8gdRb6ahN0GdbpA.png">

    </div>
    
    <h2>More</h2>
    <div class="tech-display">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/3/30/Java_programming_language_logo.svg/800px-Java_programming_language_logo.svg.png" alt="">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Microsoft_.NET_logo.svg/2048px-Microsoft_.NET_logo.svg.png">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Csharp_Logo.png">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/.NET_Core_Logo.svg/768px-.NET_Core_Logo.svg.png">

    </div>


</div>

</template>

<style scoped>

.tech-display{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
      justify-content: space-evenly;
    justify-items: center;
    align-content: space-evenly;
    align-items: center;
    

}

.tech-display > img{
    width: 8dvw;
    object-fit: contain;
    aspect-ratio: 1/1;
    padding: 1em;
    mix-blend-mode:  darken;

}
.title{
    font-weight: 400;
    font-size: 1.2em;
}
.d-palette{
    border-radius: 16px;
    width: fit-content;
    margin: 0 auto;
    padding: 1.75em 5em;
    border: 3px solid black ;
    transition: all .5s;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 30px;
    -webkit-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(191, 179, 179, 0.28);

    
    }
</style>