<template>
<div class="hire-me" id="hireme" >
     <h1>What I Offer</h1>
<p> 
 <strong style="font-size: 1.2em;"></strong><br>
  🌟 <strong>Availability:</strong> I'm currently open to new projects and opportunities.<br>
  🌐 <strong>Flexibility:</strong> Whether it's full-time employment, freelance work, or short-term contracts, I can adapt to your needs.<br>
  💲 <strong>Competitive Rates:</strong> My rates are competitive, and I offer value-driven solutions.<br>
  🚀 <strong>Quick Response:</strong> I prioritize clear communication and respond promptly.<br>
</p>
</div>
<div class="hire-me">
<h2>Get in touch</h2>
<p>Let's connect! Here are the ways you can reach me:</p>
<ul class="communication-list">
  <li>
    <i class="fas fa-envelope"></i>
    <a href="mailto:mohamedrayenzaafouri@gmail.coù">Email</a>
  </li>
  <li>
    <i class="fab fa-whatsapp"></i>
    <a href="https://wa.me/+21622231494">WhatsApp</a>
  </li>
  <li>
    <i class="fab fa-linkedin"></i>
    <a href="https://www.linkedin.com/in/mohammed-rayen-zaafouri-670360253/">LinkedIn</a>
  </li>
</ul>


</div>

</template>

<style scoped>

.communication-list{
    list-style-type: none;

}

i{    margin-right:1em ;
}

a {
    all: unset;
    cursor: pointer;
}
.hire-me{
    border-radius: 16px;
    width: fit-content;
    margin: 0 auto;
    padding: 1.75em 5em;
    border: 3px solid black ;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 30px;
    -webkit-backdrop-filter: blur(5px);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(191, 179, 179, 0.28);
    margin-top: 1em;
    max-width: 50dvw;

    animation: cardReveal 2s forwards;

    }
    @keyframes cardReveal{
    from {
        scale: 0.5;
        transform: translateY(100px);
    }
    to {
            scale: 1;
        transform: translateY(0);
    }
    }

</style>