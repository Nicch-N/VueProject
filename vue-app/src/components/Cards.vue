<template>
    <div class="bg">
        <div class="cardContainer">
            <div class="scrollBar">
                <div class="cardItem" v-for="index in 2" :key="index">
                    <div class="cardTitle">Card Item!</div>
                    <div class="cardContent">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem, deserunt voluptate! Quaerat suscipit aut iusto, atque eum veniam consectetur corporis. Qui labore provident repudiandae veritatis ab magni harum rem unde!</div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
    *{
        margin: 0px;
    }
    .bg{
        background-color: rgb(59, 59, 59);
    }
    .scrollBar{
        overflow: auto;
        display: flex;
        flex-flow: row;
        padding: 10px 30px;
    }
    .cardContainer{
        margin: auto;
        width: fit-content;
        max-width: 50%;
        border: 2px solid rgb(211, 211, 211);
        border-radius: 10px;
        display: flex;
        flex-flow: row;
        overflow: hidden;
    }
    .cardItem{
        background-color: rgb(255, 255, 255);
        width: 300px;
        height: fit-content;
        border-radius: 5px;
        padding: 5px;
        margin: auto 5px;
        min-width: 300px;
    }
    .cardTitle{
        border-bottom: 2px solid rgba(153, 153, 153, 0.692);
    }
    .cardContent{
        margin-top: 10px;
    }
</style>
<script>
    export default{
        name:'CardsCssTest'
    }
</script>