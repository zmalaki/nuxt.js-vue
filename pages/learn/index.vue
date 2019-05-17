<template>
  <section class="boxs">
       <Learn
       v-for="text in text"
       :key="text.id"
       :thumbnali="text.thumbnali"
       :title="text.title"
       :previewtext="text.previewtext"
       :id="text.id"
       />
  </section>
</template>
<script>
import Learn from '@/components/learn'
import { Promise, resolve, reject } from 'q';
import thumbnali from "~/assets/vue.png";
export default {
components:{
  Learn
},
asyncData() {
  return new Promise((resolve,reject)=>{

      resolve({
      text:[{
         thumbnali,
          title:"vue.js",
          previewtext:"SPA ",
          id:"1",
          },
        {
          thumbnali,
          title:"nuxt.js",
          previewtext:"SPA",
          id:"2",
        }
      ]
    })

  })

}

};
</script>

<style scoped>
.boxs{
  display: flex;

  flex-flow: row wrap;
  justify-content: center;
}

</style>

