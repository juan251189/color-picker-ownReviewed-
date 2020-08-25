<template>
  <div id="app">
    <headerColors :color="color"/>
    <colorPicker :colors="colors" v-on:pickColor="pickCol" />
    <gridColors :color="color"></gridColors>
  </div>
</template>

<script>
import headerColors from "./components/headerColors.vue";
import colorPicker from "./components/colorPicker.vue";
import gridColors from "./components/grid-colors.vue";

export default {
  name: "App",
  components: {
    headerColors,
    colorPicker,
    gridColors
  },
  data(){
    return{
      colors:["#7a033a","#8f8743","#c7578f","#6aa146","#62299f","#a68a49"],
      color: ""
    }
  },

  methods: {
    pickCol(e) {
      this.color=e;
      
    }
  }
};
</script>

<style>
body{
  margin:0;
  padding: 0;
}
</style>
