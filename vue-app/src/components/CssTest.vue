<template>
    <div class="mid">
        <button class="button" v-for="button in buttonList" :key="button">
            {{button}}
        </button>
        <!-- <TargetComponent/> -->
    </div>
</template>

<style>
    .mid{
        margin: 0px;
        width: 100%;
        height: 100%;
        background-color: rgb(54, 54, 54);
    }
    .button{
        margin: 5px;
        padding: 10px;
        border-radius: 10px;
        transition: .25s;
        border-top: 2px;
        border-left: 2px;
        border-right: 2px;
        border-bottom: 2px;
        border: solid rgb(26, 26, 31);
        background-color: white;
    }
    .button:hover{
        border-radius:5px;
        box-shadow: 0px 2px 1px 1px rgb(94, 94, 94);
        transform: scaleX(1.1);
        
    }
    
</style>

<script>
    const buttons = [
        'Hi',
        'There',
        ':)'
    ]
    export default{
    name: "CssTest",
    data() {
        return {
            buttonList: buttons
        };
    }
}
</script>