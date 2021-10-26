<template>
  <div class="link" v-bind:class="{ active: isActive }">
   {{name}}
  </div>
</template>

<script>
export default {    
  name: 'Link',
  props: {
    name: String,
    isActive:Boolean
  } ,
}
</script>
<style scoped>
.link{ 
    text-align: left;
    font-size: 14px;
    line-height: 17px;
    border-bottom: 1px solid tomato;
    color:tomato;
    cursor: pointer;
  }
.active{
  color: SteelBlue;
  border-bottom: 1px solid SteelBlue;
 }
</style>