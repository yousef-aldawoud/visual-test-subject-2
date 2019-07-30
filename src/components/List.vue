<template>
    <div>
        <h1>HhdawFAWCVUDWA</h1>
        <input type="text" name="input" v-on:keyup.enter="addItem" id="input" v-model="inputValue" ><span class="plus-icon" @click="addItem">+</span>
        <div class="error">{{error}}</div>
        <hr style="width:50%">
        <Item v-on:delete="deleteItem(index)" :icon-index="iconIndex" v-for="( item,index) in items" :key="index" :text="item"></Item>
    </div>
</template>
<script>
import Item from "./Item";
export default {
    components:{
        Item,
    },
    data(){
        return{
            iconIndex:0,
            error:"",
            inputValue:"",
            items:[
            ]
        }
    },methods:{
        deleteItem(index){
            this.items.splice(index, 1);
        },
        addItem(){
            if(this.inputValue ===""){
                this.error = "WADcdgjihseofvEWADwau";
                return;
            }
            this.items.push(this.inputValue);
            this.inputValue = "";
            this.error = "";
        }
    },mounted(){
         this.iconIndex = Math.floor(Math.random()*(2)+0);
    }
}
</script>
<style scoped>
.error{
    color:red;
    margin: 20px;
}
.plus-icon{
    margin-left:5px; 
    color:green;
    font-size: 20pt;
    cursor: pointer;
}
</style>
