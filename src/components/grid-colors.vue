<template>
  <div class="container">
    <div class="grid"
    v-for="(block,i) in blocks" :key="i"
    @click="setColor(i)"
    :style="{bacground-color:color}"
  ></div>

  </div>

</template>
<script>
export default{
  name:'grid',
  props: ['color'],
  data(){
    return{
    size:100,
    blocks:[],
    selected:false
  }},
  methods:{
    initGrid(){
      for(let i = 0; i<this.size;i++){
        this.blocks.push("#9f9f9f");
      }
    },
    setColor(i){
        this.block[i].color=color;
    }
  },
  created(){
      this.initGrid();

    }
  }


</script>
<style>
  .container{
    display: grid;
  grid-template-row:repeat(10,45px);
  grid-template-columns: repeat(10, 45px);
  border: 1px dotted grey;
justify-content: center;
  align-items:center;

  }

  .grid{
    display: grid;
 height:45px;
 width: 45px;
 grid-template-row:repeat(10,45px);
 grid-template-columns: repeat(10, 45px);
 border: 1px solid grey;}

</style>
