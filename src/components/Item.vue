<template>
    <div class="item">
        - {{text}} <i @click="deleteItem"  :class="icons[iconIndex]" aria-hidden="true"></i>
    </div>
</template>
<script>
export default {
    data(){
          return {
              icons:['delete-icon fa fa-trash-o','delete-icon fa fa-times','delete-icon fa fa-times'],
          }
    } ,
    props:{
        iconIndex:{default:0},
        index:{default:0},
        text:{type:String,defualt:""}
    },
    methods: {
        getIcon(){
            
        },

      deleteItem(){
          this.$emit("delete");
      }
    },
}
</script>
<style scoped>
.item{
    font-size: 20pt;
}
.delete-icon{
    color:red;
    cursor: pointer;
}

</style>
