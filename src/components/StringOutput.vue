<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1 {
        margin-top: 10px;
        color: rgb(204, 0, 255);
        text-align: center;
        padding: 10px;
    }
</style>
