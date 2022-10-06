<script>
    export default{
        name:'TargetComponent'
    }
</script>
<style>
    .target{
        --size : 40px;
        border-radius: 100%;
        width: var(--size);
        height: var(--size);
        border-style: solid;
        border-color: red;
        border-width: calc(0.2*var(--size));
        transition: .2s;
        background-color: white;
    }
    .target:hover{
        background-color: antiquewhite;
        border-color: rgb(110, 24, 150);
    }
</style>
<template>
    <button class="target"/>
</template>