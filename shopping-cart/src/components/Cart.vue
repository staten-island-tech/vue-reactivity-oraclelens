<template>
    <button><slot></slot></button>
</template>

<script>
    export default {
        name: "CartButton",
    }
</script>

<style scoped>
    button{
        width:200px;
        font-size: 15px;
        border: 10px white;
        border-radius: 50px;
        background-color: rgb(43, 66, 43);
        color:white; 
        height: 50px;   
        margin: auto;  
        transition: 0.5s;   
    }
    button:hover{
        transform: scale(1.1);
    }
    button:active{
        transform: scale(0.9);
    }
</style>