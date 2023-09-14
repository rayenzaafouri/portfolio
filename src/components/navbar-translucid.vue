<template>
    <nav>
        <div>
            <a>
                Overview
            </a>
            <a>
                Projects
            </a>
            <a>
                Curriculum Vitae
            </a>
        </div>
        </nav>
</template>

<style scoped>
nav {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    top: 0;
    z-index: 2;

}

nav > div{
    width: fit-content;
    padding: 16px;
    margin: 5px;
    border-radius: 16px;
    background-color: rgba(255, 255, 255, .15);  
    backdrop-filter: blur(5px);
    padding: 16px;
    border: 1.75px solid grey;


}

</style>
