<template>
  <div id="app">
  
    <WebViewer :path="`${publicPath}webviewer`" url="./test-test.docx"/>

    <!-- <v-btn @click="clickme">
      click
    </v-btn> -->
  </div>
</template>

<script>
import WebViewer from '@/components/WebViewer.vue'
export default {
  name: 'app',
  components: {
    WebViewer
  },
  data () {
    return {
      publicPath: process.env.BASE_URL,
      url:"",
    }

  },

  methods: {
    // clickme(){
    //   const a = document.createElement("a");
    //   a.setAttribute("target", "_blank");
    //   a.setAttribute("href", "./doc1.docx");
    //   a.click();
    // }
    
  },

  mounted(){
    // const blob = new Blob(
    // //     [new Uint8Array([...base64].map((char) => char.charCodeAt(0)))],
    // //     { type: "application/pdf" }
    // //   );
    // const objectUrl = window.URL.createObjectURL(new Blob([base64]));
    // // const objectUrl = window.URL.createObjectURL(blob);
    // this.url=objectUrl
}
}
</script>


<style>
html,
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0 auto;
  height: 100vh;
}
#webviewer{
  height: 100vh;
}
</style>