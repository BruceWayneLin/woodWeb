<template>
  <div id="app">
    <router-view></router-view>
    <footer>
      <div class="col-xs-12 text-left">
        <p>Copyright © 2017 林業試驗所   木材標本館。</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app'
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
footer {
  margin-top: 60px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 50px;
}
footer p {
  color: white;
  vertical-align: middle;
  position: absolute;
  top: 15px;
}
</style>
