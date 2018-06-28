<template>
  <div id="app">
    <Navheader/>
       <router-view></router-view>
    <Navfooter/>
  </div>
</template>
<script>
import Navfooter from '@/components/Navfooter.vue'
import Navheader from '@/components/Navheader.vue'
import Home from '@/page/Home.vue'
export default {
name: 'App',
  components: {
    Navfooter,
    Navheader,
    Home
  }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  margin: 0;
  padding: 0;
  font-family: 微软雅黑;
}
a {
  text-decoration: none;
}

input {
  outline: none;
}

li {
  list-style: none;
}

body {
  background: #f5f4f5;
  font-size: 14px;
  color: #333;
  display: block;
}
</style>
