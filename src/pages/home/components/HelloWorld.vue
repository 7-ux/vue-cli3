<template>
  <div class="hello">
    <h4>{{ msg }}</h4>
    <br>
    <hr>
    <br>
    <p v-square="16"></p>
    <!-- 使用指令 v-focus -->
    <input type="text" v-focus />
    <br>
    <hr>
    <br>
    <!-- 点击按钮，会触发时间patch -->
    <button type="button" name="button" @click="$emit('patch', 22)" >发送数据到父组件</button>
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
