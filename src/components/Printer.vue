<template>
  <div class="printer">
   <Node  msg="Node" :el='json'/>
  </div>
</template>

<script>
import Node from './Node.vue'
// import Sheet from './Sheet.vue'
import json from '../../public/static/node_modules.json'
console.log(json);
Object.freeze(json)
export default {
  name: 'Print',
  components: {
    Node, 
  },
  data:()=>({json})

}
</script>
<style scoped>
</style>