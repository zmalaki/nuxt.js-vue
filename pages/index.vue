<template>
  <section>
    <h1 >what is vue.js?</h1>
    <p class="subheading">
      Vue.js lets you extend HTML with HTML attributes called directives
      <br>Vue.js directives offers functionality to HTML applications
      <br>Vue.js provides built-in directives and user defined directives
      <br>
    </p>
      <ul class="vue">

        <li v-for="user in users" :key="user.id">
              <NuxtLink :to="'/'+user.id">
                {{ user.name }}
              </NuxtLink>
        </li>

    </ul>

    <h1>what is nuxt.js?</h1>
    <p class="subheading">
      Its main scope is UI rendering while abstracting away the client/server distribution.<br>
      Our goal is to create a framework flexible enough that you can use it as a main project <br>base or in addition to your current project based on Node.js.
      Nuxt.js presets all the configuration needed to make your development of a server-rendered<br> Vue.js Application more enjoyable.
      In addition, we also provide another deployment option called: nuxt generate. It will build<br> a statically generated Vue.js Application. We believe that option could be the next big step in the development of Web Applications with microservices.
    </p>


  </section>


</template>


<script>
export default {
  transition: 'bounce',
   asyncData({ env }) {
    return { users: env.users }
  }

}
</script>

<style>
.vue{  list-style-type: none;
  margin: 0;
  padding: 0;
  }

  .vue li a{
    display: block;


  text-align: left;
  color: #222;
  text-decoration: none;
  font-size: 15px;;
  }
</style>
