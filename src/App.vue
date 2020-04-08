<template>
  <div>  
     <h1>{{content2}} </h1>
     <wode content="点点击了的次数" :count="2"></wode>
     <wode content="又点击了的次数" :count="0"> </wode>
     <hr/>
     <input type="text" v-model="title">
     <input type="text" v-model="content">
     <input type="button" @click="addArticle" value="tmjwwfvh">
     <article v-for="(item,index) in list" :key="index" :title="item.title" :content="item.content">
       <!-- {{item.title}} {{item.content}} 错误，应该吧title和content传给组建里面-->
     </article>
  </div>
  
</template>

<script>
import My from "@/MyTemplate.vue"
import article from "@/components/articleTest.vue"
export default {
  data:()=>({
    content2:"hello World!!~",
    list:[],
    title:"",
    content:""
  }),
  components:{
    wode:My,
    article:article
  },
  methods:{
    addArticle(){
      this.list.push({
        title:this.title,
        content:this.content
      });
    }
  }
  // data:function(){
  //   return ({content:"nihao"})
  // }
}
</script>

<style>

</style>
