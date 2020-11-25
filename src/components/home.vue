<template>
    <div>
        home 组件----{{title}}
        <br>
        <button @click="changeTitle(1212)">改变title</button>
    </div>
</template>
<script lang="ts">
import {defineComponent} from 'vue'
let title:string="我是一个home组件"
export default defineComponent({
    data(){
        return {
            title
        }
    },
    mounted(){

    },
    methods:{
        setTitle():void{
            this.title='123'
        },
        changeTitle(val:string){
            this.title=val
        }
    }
})
</script>
<style lang="scss">

</style>