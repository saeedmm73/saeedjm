<!-- eslint-disable vue/no-unused-vars -->

<template>
  <q-page padding>
    <div>
      <div><q-input
       @keyup.enter="addTask"
       v-model="newTask"
       square
       filled
       placeholder="Add Task"></q-input></div>
       <q-list separator>
        <q-item v-for="(task, index) in Tasks"
        :key="task.taska"
        :index="index">
      <div><q-item-section>
       <q-item-label>{{ task.taska }}</q-item-label>
       <div><button class="but" @click="delet(index)">X</button></div>
      </q-item-section></div>
    </q-item>
       </q-list>
    </div>
  </q-page>
</template>


<script>
import { secureHeapUsed } from 'crypto';

export default {
  data() {
    return {
      newTask :'',
      Tasks : []
  }
},
methods : {
  delet(index) {
    this.Tasks.splice(index , 1)
  },
  addTask(){
      this.Tasks.push({taska: this.newTask})
      this.newTask = ''
    }
}
}
</script>



<style>
.but {
  background-color: brown;
  color: aliceblue;
  margin-left: 65vw;
  border: 0.5vw groove yellow;
  padding-block: ;
}
</style>
