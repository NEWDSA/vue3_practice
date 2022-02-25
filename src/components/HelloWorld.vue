<template>
  <div class="hello">
    <input type="text" v-model="msg" />
    <h3>Essential Links</h3>
  </div>
</template>

<script>
import {h,ref,reactive} from "vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  setup() {
    const readerNumber=ref(0);
    const book=reactive({title:'vue 3 guide'})
    //use render
    return ()=>h('canvs',[readerNumber.value,book.title])
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
