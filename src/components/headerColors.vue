<template>
  <div class="header">
    <h1 class="header-title">Color<span class="span-header">Picker</span></h1>
    <div class="picked-block" :style="'background-color:'+color+';'"></div>
  </div>
</template>

<script>
  export default{
    name:'header-colors',

  props: ['color']
}


</script>
<style>
.header{
  display:flex;
  justify-content: space-around;
  align-items: center;
  background-image: linear-gradient(to right,#182b83,#21668c);
  color:rgb(223, 226, 236);


}
.header-title{
  font-size: 38px;
  font-family: "monserrate",sans-serif;
  font-weight: 700

}
.span-header{
  color: rgb(207, 215, 39);
}

.picked-block{
  border: 3px dotted #eba630;
  width: 50px;
  height: 50px;
}
</style>
