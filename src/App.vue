<template>
  <div id="app">
    <!-- <Introduction/> -->
    <div class="container">
      {{ title }}
      <component :is="page"/>
    </div>
  </div>
</template>

<script>
// import Introduction from './content/introduction.md';
import Color from './components/Color.vue';
import CodeBlock from './components/CodeBlock.vue';

export default {
  name: 'App',
  // components: {
  //   Introduction: {
  //     extends: Introduction.vue.component
  //   } 
  // },
  data: () => {
    return {
      page: null,
      title: null
    }
  },
  created() {
    const pathname = window.location.pathname.slice(1);
    this.page = () => import(`./content/${pathname}.md`)
      .then(({ attributes, vue }) => {
        this.title = attributes.title
        return { extends: vue.component, components: { Color, CodeBlock } }
      })
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: left;
  width: 800px;
  margin: 60px auto 0;
}

code {
  background-color: #e4e4e4;
  padding: 10px;
  text-align: left;
  display: block;
}
</style>
