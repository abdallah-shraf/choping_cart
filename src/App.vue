<template>
  <div id="app">
    <div id="nav">
      <router-link :class="{ctive:$router.name ==='Home'}" to="/">Home</router-link> 
      <router-link :class="{ctive:$router.name === 'Cart'}" to="/Cart"> Cart</router-link>
    </div>
    <router-view />
  </div>
</template>
<script>
export default {
  mounted(){
    this.$store.commit('updateCartFromLocalStorage')
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html, body{
  margin: 0;
  padding: 0;
  overflow-x:hidden ;
}
body{
  background-color: rgp(245,245,245);
}

#nav {
  padding: 10px;
  width: 100%;
  height: 100%;
  background-color: #fff;
  line-height: 30px;

  a {
    font-weight: bold;
    color: darkgray;
    text-decoration: none;
    margin: 0 5px 0 5px ;
    font-size: 1.5rem;
    
    &.active{
      color: #2c3e50;
    }
  }

  .text-center{text-align: center;

  }
  
}
</style>
