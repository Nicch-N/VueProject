<script>
    export default{
        name:'NavBar',
        props:{
            routeLinks: { type: Object, required: true },
            test:{type:String}
        },
        data(){
          return {
            routes:this.routeLinks
          }  
        },
        created() {
            // props are exposed on `this`
            // console.log(this.routeLinks)
            // console.log(this.test)
        }
    }
</script>
<style>
    .navBar{
        width: 100vw;        
        border-bottom: 1px solid rgba(163, 163, 163, 0.178);
        display: flex;
        padding: 10px 5px 10px 30px;
        background: linear-gradient(rgb(255, 255, 255), rgb(199, 199, 199));;
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
    .navItem:hover{
        background-color: rgb(180, 180, 180);
        border-radius: 15%;        
    }
</style>
<template>
    <div class="navBar">
        <!-- {{Object.values(routes)}} -->
        <a class="navItem" :href="routes.HelloWorld">A</a>
        <a class="navItem" :href="routes.HelloThere">B</a>
        <a class="navItem" :href="routes.CssTest">C</a>
    </div>
</template>