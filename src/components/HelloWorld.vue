<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      antdv组件UI2.0规范前端修改代码
      <br />
      点击查看
      <a href="https://github.com/DS-teacher/MyAntdv" target="_blank" rel="noopener">
        源码位置
      </a>
      。
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #42b983;
}
</style>
