<template>
    <div>
        {{getContent}} 
        <button @click="addNum">+1</button>
    </div>
</template>

<script>
export default {
    data:()=>({
        count:0
    }),
    methods:{
        addNum(){
            this.count++;
            }
    },
    computed:{
        getContent(){
            return this.content+this.count;
        }
    },
    props:{
        content:{
            type:String,
            required:true
        },
        count:{
            type:Number
        }
    }
}
</script>
