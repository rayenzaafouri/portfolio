<template >
    <div class='dev-intro'>
        <img :src="require('@/assets/pic.jpg')" alt="">
        <h2>Rayen</h2><h2>Zaafouri</h2>
        <div class="overview-p">
            <p>Experienced software developer with expertise in creating robust and scalable solutions.</p>
        </div>


    </div>
</template>

<script>
export default {
    
    /*
    

.dev-intro {
    margin-top: 16px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    background: white;
    border-radius: 16px;
    padding: 1.5em;
    border: 4px solid black;
    width: fit-content;
    position: relative;
    margin: 0 auto;


}

img {

    height: 150px;
    aspect-ratio: 1/1;
    border-radius: 100%;
    padding: 5px;
    border: 2px solid green;
}*/
}
</script>


<style scoped>
    .dev-intro{
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-top:55dvh ;
    }
    .dev-intro > div {
        position: absolute;
        top: 60dvh;
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


