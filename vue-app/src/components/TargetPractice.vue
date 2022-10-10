<template>
    <TargetComponent class="target"/>
</template>

<style>
    .target{
        height: 40px;
        width: 40px;
    }
</style>

<script>
    import TargetComponent from './TargetComponent.vue'
    const buttons = [
        'Hi',
        'There',
        ':)'
    ]
    export default{
    name: "TargetPractice",
    data() {
        return {
            buttonList: buttons
        };
    },
    components: { TargetComponent }
}
</script>