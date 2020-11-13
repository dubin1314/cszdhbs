<template>
  <div id="app">
    <el-container>
      <el-main  class="maxWidth">
         <d-header></d-header>
         <d-container></d-container>
      </el-main>
      <el-footer class="footer" >
        <d-footer  class="maxWidth"></d-footer>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
import dHeader from './components/dHeader.vue'
import dContainer from './components/dContainer.vue'
import dFooter from './components/dFooter.vue'

export default {
  name: 'App',
  components: {
    dHeader,dContainer,dFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.maxWidth{
  max-width: 1200px;
  margin:0 auto;
}
#app .footer{
   background: #28b28b;
  height: 224px !important;
}
</style>
