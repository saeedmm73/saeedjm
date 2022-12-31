<template>
  <div class="colo">
    <h2 id="bold">session one</h2><br/>
    <p>Hello {{ name }} {{ lastname }}, we are learning vue! it is freaking hard</p>
    <input :value="name" @input="clickon()" ref="zz">
    <input :value="lastname" @input="clickon()" ref="la">
  </div>
</template>
<style scoped>
.colo {
  background-color: blue;
  padding: 10px;
  color: aliceblue;
}
#bold {
font-weight: bold;
}
</style>

 <script>
  export default {
    name:"v1",
    data() {
      return {
        name : "saeed",
        lastname : "moqadam",
      }
    },
    methods : {
      clickon() {
        this.name = this.$refs.zz.value;
        this.lastname = this.$refs.la.value
      }
    }

  }
 </script>
