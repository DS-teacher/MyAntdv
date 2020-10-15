<template>
  <a-layout id="components-layout-demo-top" class="layout">
    <a-layout-header>
      <div class="logo" />
      <a-menu
        theme="dark"
        mode="horizontal"
        :defaultSelectedKeys="['2']"
        :style="{ lineHeight: '64px' }"
      >
        <a-menu-item key="1">nav 1</a-menu-item>
        <a-menu-item key="2">nav 2</a-menu-item>
        <a-menu-item key="3">nav 3</a-menu-item>
      </a-menu>
    </a-layout-header>
    <a-layout-content style="padding: 0 50px">
      <a-breadcrumb style="margin: 16px 0">
        <a-breadcrumb-item>Home</a-breadcrumb-item>
        <a-breadcrumb-item>List</a-breadcrumb-item>
        <a-breadcrumb-item>App</a-breadcrumb-item>
      </a-breadcrumb>
      <div :style="{ background: '#fff', padding: '24px', minHeight: '480px' }">
        <div>
          <a-space direction="vertical">
            <a-space>
              <a-button type="primary" :size="large">
                Primary
              </a-button>
              <a-button :size="small">
                Normal
              </a-button>
              <a-button icon="search">
                Search
              </a-button>
            </a-space>
            <a-date-picker @change="onChange" />
            <a-month-picker placeholder="Select month" @change="onChange" />
            <a-range-picker @change="onChange" />
            <a-week-picker placeholder="Select week" @change="onChange" />
          </a-space>
        </div>
      </div>
    </a-layout-content>
    <a-layout-footer style="text-align: center">
      Ant Design ©2020 Created by Ant UED
    </a-layout-footer>
  </a-layout>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  methods: {
    onclick() {
      console.log(123);
    },
    onChange(date, dateString) {
      console.log(date, dateString);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
