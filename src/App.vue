<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name : 'About'}">About</router-link> | <!-- bind to the component : good practice to use as it would help if I change the paths in the future-->
  <router-link :to="{ name : 'Jobs'}">Jobs</router-link>
  </div>
  <!--  <router-view/> : this is where the component is injected -->
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
