<template>
  <header>
    <ul>
      <li><nuxt-link to="/" >Starting page</nuxt-link></li>
      <li><nuxt-link to="/learn" >Learn</nuxt-link></li>
      <li><nuxt-link to="/about" >About</nuxt-link></li>
    </ul>
  </header>
</template>
<style>
header{
  width: 100%;
  background-color: rgb(196, 191, 185);
  width:100%;
  height:30px;
  display:flex;
  justify-content:center;
  align-items: center;
  padding: 2em;
}

  ul{
    list-style:none;
    padding:0;
    margin:0;
    display:flex;
    justify-content:center;
    align-items:center;

    }

    li{
      font-size: 2em;
      margin:0 10px;

    }
    a:hover{
      text-decoration: none;
      font-size: 20px;
       font-size: 1em;
         margin:0 10px;


    }

</style>


