<template>
    <div class="mid">
        <button class="button">Press me!</button>
    </div>
</template>1

<style>
    .mid{
        display: flex;
        flex:1 1 auto;
        size: 100%;
        color: black;
        background-color: black;
    }
    .button{
        padding: 20px;
        size: 30px 30px;
        margin-left: auto;
        margin-bottom: 50%;
        margin-right: 50%;
        margin-top: 50%;
        border-radius: 40%;
    }
    .button:hover{
        background-color: blue;
    }
</style>

<script>
    export default{
        name:'CssTest'
    }
</script>