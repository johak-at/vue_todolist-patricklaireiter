<script setup>
import { ref } from "vue";
const list = ref([])
const newItem = ref("");
 function addItem(){
list.value.push(newItem.value);
newItem.value = "";  

}
function deleteItem(){
newItem.value = "";  
}

</script>

<template>
  <h1>TodoList</h1>
    <input type="text" v-model="newItem" placeholder="neue Aufgabe" />
<button @click="addItem">Add</button>
<ul>
    <li v-for="item in list" :key="item">{{item}}</li></ul>
    <button @click="deleteItem">Delete</button>
</template>