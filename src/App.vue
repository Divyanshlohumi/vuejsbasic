<template>
  <div id="app">
    <header class="header">
      <h1>String Transform</h1>
    </header>
    <StringTransform v-on:change-string="changeString"/>
    <StringOutput v-bind:msg="msg"/>
  </div>
</template>

<script>
import StringTransform from './components/StringTransform.vue'
import StringOutput from './components/StringOutput'
export default {
  name: 'App',
  components: {
    StringTransform,
    StringOutput
  },
  data() {
    return {
      msg: ""
    }
  },
  methods: {
    changeString(s){
      this.msg = s
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.btn {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}

.btn:hover {
  background: #666;
}

.header {
  background: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
}
</style>
