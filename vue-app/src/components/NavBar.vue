<script>
    export default{
        name:'NavBar',
        props:{
            routeLinks: { type: Array, required: true },
            test:{type:String}
        },
        data(){
          return {
          }  
        },
        created() {
            // props are exposed on `this`
            console.log(this.routeLinks)
            console.log(this.test)
        }
    }
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
        padding: 5px 0;
        display: inline;
        text-align: center;
        color: black;
        font-style: normal;
        text-decoration: none;
    }
    .navItem :hover{
        background: rgb(189, 189, 189);
    }
</style>
<template>
    <div class="navBar">
        <a class="navItem" href="">A</a>
        <a class="navItem" href="">B</a>
        <a class="navItem" href="">C</a>
    </div>
</template>