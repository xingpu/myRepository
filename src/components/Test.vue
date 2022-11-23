<template>
    <div class="container">
        <div>坐标</div>
        <div>x: {{x}}</div>
        <div>y: {{y}}</div>
    </div>
</template>
<script>
    import { onMounted, onUnmounted, reactive, ref, toRefs} from 'vue'
    export default {
        name: 'App',
        setup () {
            let mouse=reactive({
                x:0,
                y:0
            })
            const move=(e)=>{
                mouse.x=e.pageX
                mouse.y=e.pageY
            }
            onMounted(()=>{
                document.addEventListener('mousemove',move)
            })
            return { ...toRefs(mouse),move}
        }
    }
</script>
<style scoped lang="less"></style>