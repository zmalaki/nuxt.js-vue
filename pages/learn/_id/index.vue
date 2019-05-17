<template>
<section class="single-vue">
  <h1>{{text.id}}</h1>
  <div>
    <img class="vue-img" :src="text.thumbnali" alt="">
  </div>
  <p>{{ text.description}} </p>
</section>
</template>
<script>
import thumbnali from "~/assets/vue.png"
export default {
  asyncData(contaxt) {
  return new Promise((resolve,reject)=>{

      resolve({
      text:[
        {
         thumbnali,
          title:"vue.js",
          previewtext:"FrameWork",
          id:"1",
          description:"Use for single page application",
        },

        {
           thumbnali,
          title:"nuxt.js",
          previewtext:"FrameWork",
          id:"2",
          description:"Use for single page application",
        }
      ].find(el => el.id === contaxt.params.id)
    })

  })

}

}
</script>

<style scoped>
a{
  text-decoration: none;
  color: black;
}
.single-vue{
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
.vue-img{
  width: 100%;
  height: 200px;
}
</style>
