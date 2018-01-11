<template>
  <div id="app">
    <vue-qr :text="text" :autoColor='true' :logoSrc="src2" :size="400" :margin="0"></vue-qr>
    <vue-qr text="Hello worlduhefiuehifu!" :autoColor='true' :bgSrc="src" :logoSrc="src2" :size="400" :margin="0" style="margin-top:30px">
    </vue-qr>
  </div>
</template>

<script>
import VueQr from 'vue-qr'
export default {
  name: 'app',
  components: {
    VueQr
  },
  data() {
    return {
      src: require('./assets/bg1.png'),
      src2: require('./assets/avatar.png'),
      text: '0adiaudfsdfsdiu'
    }
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
  margin-top: 60px;
}
</style>
