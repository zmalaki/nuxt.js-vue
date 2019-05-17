<template>
<nuxt-link :to="'/learn/' + id">
    <article class="box">
      <div class="thumbnali"  :style="{ backgroundImage: 'url('+ thumbnali +')' }"></div>
      <h1>{{ title }}</h1>
      <p>{{ previewtext }}</p>
    </article>
 </nuxt-link>
</template>
<script>

export default {
  props:[ 'thumbnali','title','previewtext','id']
}
</script>

<style>
.box{
  border: 1px solid gray;
  box-sizing: 380px;
  padding: 8px;
  box-shadow: 0 2px 2px gray;
  margin: 10px;

}
.thumbnali{
  background-position: center;
  background-size: cover;
  width: 300px;;
  height: 200px;
}
</style>
