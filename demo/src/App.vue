<template>
  <div id="app">
    22
    <vue-qr text="Hello world!"
            :autoColor='true'
            :bgSrc="src"
            :logoSrc="src2"
            :size="200"
            :sizes="[400,800]"
            :pos="[100,300]"
            :margin="0"
            style="margin-top:30px"
            :dotScale="0.35">
    </vue-qr>
  </div>
</template>

<script>
import VueQr from "../../src/main"
export default {
  name: "app",
  components: {
    VueQr
  },
  data() {
    return {
      src:
        "https://upload.emeker.com/?key=82add1c07e8816370e69708d0785548371b59f55&token=b586a7b4df293756527e932b513b169766e78c8aca13cbfdbcb90cf1128954c9d0afe7b579c49975911c3bb6ad06aace:a8be87e2deb3976f586a79132173eb5d",
      src2: require("./assets/avatar.png"),
      text: "testtttt",
      testNumber: "0",
      colorLight: "#fff"
    }
  },
  mounted() {
    setInterval(() => {
      const num = Number(this.testNumber) + 1
      this.testNumber = String(num)
    }, 500)
  }
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
