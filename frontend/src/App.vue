<template>
<div>
<NavBar/>
<body>
  <Swipe/>
</body>
</div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import Swipe from './components/Swipe.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    Swipe,
  }
}
</script>

<style>
/*#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
*{
    margin: 0;
    padding: 0;
    font-family: 'Rubik', sans-serif;
}
.main{
    width: 100%;
    height: 100vh;
    display: grid;
    overflow: hidden;
}

</style>
