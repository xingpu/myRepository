<template>
    <h1>子组件</h1>
    {{person.name}}
    {{person.age}}
</template>

<script>
    export default {
        name: "Son",
        props:{
          person:{
              type:Object,
              default:{}
          }
        },
        setup(props){
            props.person.age=16
        }
    }
</script>

<style scoped>

</style>