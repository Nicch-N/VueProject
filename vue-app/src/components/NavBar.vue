<script>

</script>
<style>
    .navBar{
        border-bottom: 1px solid rgba(163, 163, 163, 0.178);
        display: flex;
        padding: 10px 5px 10px 30px;
        background: linear-gradient(rgb(255, 255, 255), rgb(241, 241, 241));;
    }
    *{
        margin: 0px;
        margin-top: 0px;
    }
    .navItem{
        margin-right: 50px;
        width: 50px;
        display: flex;
        text-align: center;
        background: black;
    }
    .navLink{
        text-align: center;
    }
    .navItem :hover{
        font-style: italic;
        background: blue;
    }
</style>
<template>
    <div class="navBar">
        <div class="navItem">
            <a class="navLink">A</a>
        </div>
        <div class="navItem">
            <a class="navLink">B</a>
        </div>
        <div class="navItem">
            <a class="navLink">C</a>
        </div>
    </div>
</template>