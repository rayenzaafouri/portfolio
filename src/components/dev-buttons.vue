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
    border: 4px solid black;
    width: fit-content;
    position: relative;
    margin: 0 auto;
    transform: scale(75%);


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


