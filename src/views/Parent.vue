<template>
    <h1>父组件</h1>
    <Son :person="person"/>
</template>

<script>
    import Son from "./Son";
    import {reactive} from 'vue'
    export default {
        name: "Parent",
        components: {Son},
        setup(){
            let person=reactive({
                name:'likui'
            })
            return {person}
        }
    }
</script>

<style scoped>

</style>