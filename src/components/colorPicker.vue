<template>
<div class="colors-bar">
  <div class="colors-block"
    v-for="(color,i) in colors" :key="i" :style="'background-color:'+color+';'"

    v-on:click="pickColor(color)"></div>
</div>

</template>


<script>
  export default{
    name:'color-picker',
    props:['colors'],



    methods:{
      pickColor(color){
        this.$emit('pickColor',color);
      }
    }
  }

</script>

<style>
  .colors-bar{
    width: auto;
margin:20px 0;
    display: flex;
    flex:wrap;
    justify-content: center;
  }

  .colors-block{
    height: 50px;
    width: 50px;
    border:1px solid black;
  }

</style>
