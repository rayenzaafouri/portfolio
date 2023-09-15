<template >
    <div class='dev-buttons'>

        <a href="#">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/aa/LinkedIn_2021.svg/1920px-LinkedIn_2021.svg.png" alt="Add me on Linkedin">
        </a>
        <a href="#">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/GitHub_Invertocat_Logo.svg/1024px-GitHub_Invertocat_Logo.svg.png" alt="Add me on Linkedin">
        </a>
        <a href="#">
            <img :src="disquette" alt="Add me on Linkedin">
        </a>

    </div>
</template>

<script>

export default {
    data(){
        return {
            disquette : require("@/assets/disc.png")
        }
    }
}
</script>


<style scoped>



.dev-buttons {
   
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    background: white;
    border-radius: 16px;
    padding: 1.5em;
    width: fit-content;
    position: relative;
    margin: 0 auto;
    transform: scale(75%);
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
    height: 30dvh;


}

a {

    height: 5em;
    aspect-ratio: 1/1;
    border-radius: 8em;
    display: flex;
    align-items: center;
    border: 3px solid black;
    padding: .5em;

}
img{
    max-height: 100%;
    max-width: 100%;
}
</style>


