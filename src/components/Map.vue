<template>
  <div class="map">
      <div class="node">Directory</div>
      <div class="link">Link</div>
      <div class="file">File</div>
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
.map{ 
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-gap:10px;margin-bottom: 20px;
 }
 .file{
    font-size: 14px;
    line-height: 17px;
    color:DarkSlateGray;
 }
 .link{
    font-size: 14px;
    line-height: 17px;
    border-bottom: 1px solid tomato;
    color:tomato;
 }
 .node{
      border: 1px solid royalblue;
    background: none;
    color:royalblue;
    font-size: 14px;
    line-height: 17px;
 }

</style>