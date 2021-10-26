<template>
  <div class="node">
        <div class="node-next" v-if="el.type==='directory'"> 
           <button class="node-next-button" v-bind:class="{ active: isActive }" v-on:click='changeVisiability'>
              {{el.name}}
           </button>
           <div  class="node-list" v-if="visible">
                <div v-for="item in el.contents" v-bind:key="item.name">
                    <Node :el='item'/>
                </div> 
           </div>
        </div>
        <div v-else>
           <Sheet :el='el'/>
        </div>
  </div>
</template>
<script>
import Sheet from './Sheet.vue'
export default {
    
  name: 'Node',
  props: {
    msg: String,
    el:Object,
    
  },
  data:()=>({
    visible: false,
    isActive:false
  }),
   components: {
    Sheet, 
  },
  methods:{
    changeVisiability: function()
        { 
          this.isActive=!this.isActive
          return  this.visible  = !this.visible
        }
    }
}
</script>
<style scoped>
  .node-next{
    display: flex;
    align-items: flex-start;
  }
  .node-next-button{
    outline: none;
    border: 1px solid royalblue;
    background: none;
    color:royalblue;
    font-size: 14px;
    line-height: 17px;
    cursor: pointer;
  }
  .node-list{
    margin-left: 10px;
    display: grid;
    grid-gap: 5px;
    grid-template-columns: minmax(max-content, auto) minmax(max-content,  auto) minmax(max-content, auto);
    border: 1px solid rgba(108, 156, 174, 0.72);
    padding: 3px;
    border-radius: 5px;
  }
  .active{
      background: rgba(176, 215, 218, 0.549);
  }
</style>