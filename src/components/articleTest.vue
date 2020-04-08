<template>
    <div>
        <h1>{{title}}</h1>
        <p>{{content}}</p>
    </div>
</template>

<script>
export default {
    data:()=>({

    }),
    props:{
        title:{
            type:String,
            required:true
        },
        content:{
            type:String
        }
    }
    
}
</script>