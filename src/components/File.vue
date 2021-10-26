<template>
  <div class="file" v-bind:class="{ active: isActive }">
   {{name}}
  </div>
</template>

<script>
export default {    
  name: 'File',
  props: {
    name: String,
    isActive:Boolean
  } ,
}
</script>
<style scoped>
 .file{ 
    text-align: left;
    font-size: 14px;
    line-height: 17px;
    color:DarkSlateGray;
    cursor: pointer;
  }
 .active{
  color: SlateBlue;
 }
</style>