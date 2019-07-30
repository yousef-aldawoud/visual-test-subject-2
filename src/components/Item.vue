<template>
    <div class="item">
        {{text}} <i @click="deleteItem"  class="delete-icon fa fa-trash-o" aria-hidden="true"></i>
    </div>
</template>
<script>
export default {
    props:{
        text:{type:String,defualt:""}
    },
    methods: {
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
