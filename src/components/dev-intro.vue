<template >
    <div class='dev-intro' id="overview">
        <img :src="require('@/assets/pic.jpg')" alt="">
        <h2>Rayen</h2><h2>Zaafouri</h2>
        <div class="overview-p">
            <p>Experienced software developer with expertise in creating robust and scalable solutions.</p>
        </div>


    </div>
</template>

<script>
export default {
    
}
</script>


<style scoped>
    .dev-intro{
        display: flex;
        align-items: center;
        flex-direction: column;
        height: 60dvh;
        margin: 0;
    }
    .dev-intro > div {
        position: absolute;
        top: 60dvh;
    }

    h2{
        text-shadow: 0 1px 0 #CCCCCC, 0 2px 0 #c9c9c9, 0 3px 0 #bbb, 0 4px 0 #b9b9b9, 0 5px 0 #aaa, 0 6px 1px rgba(0,0,0,.1), 0 0 5px rgba(0,0,0,.1), 0 1px 3px rgba(0,0,0,.3), 0 3px 5px rgba(0,0,0,.2), 0 5px 10px rgba(0,0,0,.25), 0 10px 10px rgba(0,0,0,.2), 0 20px 20px rgba(0,0,0,.15);
    }

    img{
        position: absolute;
        margin: 0 auto ;
        top: 12dvh;
        border-radius: 100%;
        max-height: 40dvh;
        z-index: 2;
        opacity: 0.83;
    }
    h2:nth-of-type(1){
        position: absolute;
        font-size: 10em ;
        top: 30dvh;
        transform: translateX(-70%) translateY(-80%);
        word-spacing: 0;
        opacity: 0.98 ;
        color: #2c3e50;
    }
        h2:nth-of-type(2){
        position: absolute;
        font-size: 10em ;
        top: 18dvh;
        transform: translateX(24%) translateY(65%);
        word-spacing: 0;
        opacity: 0.98 ;
        color: #2c3e50;
        z-index: 3;
    }
    p{
            font-size: 1.25em;

    }

    

</style>


