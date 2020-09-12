<template>
  <div class="hello">
    <form @submit="changeString">
      <input type="text" v-model="title" name="title" placeholder="Enter String...">
      <br>
      <input type="submit" value="Transform" class="btn">
    </form>
  </div>
</template>

<script>
export default {
  name: 'StringTransform',
  data() {
    return {
      title: ''
    }
  },
  methods: {
    changeString(e) {
      e.preventDefault();
      var s=this.title.toUpperCase();
      this.$emit('change-string', s)
      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    margin-top: 10px;
  }

  input[type="text"] {
    flex: 8;
    padding: 5px;
  }

  input[type="submit"] {
    flex: 2;
  }
</style>
