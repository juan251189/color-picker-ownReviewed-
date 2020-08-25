<template>
<div class="container">
  <div class="grid" v-for="(block,i) in blocks" :key="i" @click="pickColor(i)" :style="'background-color:'+block.color+';'"></div>
</div>
</template>




<script>
export default {
  name: 'grid-color',
  props: ['color'],
  data() {
    return {
      size: 100,
      blocks: []
    }
  },
  methods: {
    initGrid() {
      for (let i = 0; i < this.size; i++) {
        this.blocks.push({
          color: '#f4f4f4'
        });
      }
    },
    pickColor(i) {
      this.blocks[i].color = this.color;
    }

  },
  created() {
    this.initGrid();
  }
}
</script>
<style>
.container {
  display: grid;

  grid-template-columns: repeat(10, 45px);

  justify-content: center;
  align-items: center;

}

.grid {
  display: grid;
  height: 45px;
  width: 45px;

  border: 1px solid grey;
}
</style>
