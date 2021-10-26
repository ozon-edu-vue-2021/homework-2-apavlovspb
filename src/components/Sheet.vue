<template>
  <div  v-if="el.type==='link'"  v-on:click='changeActive'>
    <Link :name='el.name' :isActive='isActive'/>
  </div>
  <div  v-else  v-on:click='changeActive'>
    <File :name='el.name' :isActive='isActive'/>
  </div>
</template>

<script>
import File from './File.vue'
import Link from './Link.vue'
export default {    
  name: 'Sheet',
  props: {
    el: Object
  } ,
    components: {
    Link, File
  },
  data:()=>({isActive:false}),
  methods:{
      changeActive:function(){
          return this.isActive =!this.isActive
          }
  }

}
</script>
<style scoped>
  
</style>