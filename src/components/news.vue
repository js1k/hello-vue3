<template>
    <div>
        home 组件----{{title}}
        <br>
        <button @click="setTitle">改变title</button>
        <br>
        {{reverseTitle}}
    </div>
</template>
<script lang="ts">
import {defineComponent} from 'vue'

interface News{
    title:string,
    description:string,
    count:number,
    content?:string // 可选参数
}
// let newsData:News={
//     title:"我是一个新闻",
//     description:'我是描述',
//     count:12323
// }
let newsData={
    title:"我是一个新闻",
    description:'我是描述',
    count:12323
} as News
export default defineComponent({
    data(){
        return newsData
    },
    computed:{
        reverseTitle():string{
            return this.title.split("").reverse().join("")
        }
    },
    mounted(){

    },
    methods:{
        setTitle():void{
            this.title='123'
        },
        changeTitle(){
            
        }
    }
})
</script>
<style lang="scss">

</style>