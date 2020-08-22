<template>
  <pre v-highlightjs>
    <code :class="language">
      <slot/>
    </code>
    </pre>
</template>

<script>

export default {
  name: 'CodeBlock',

  props: ['language']
}
</script>

<style>
  pre {
    margin: 0 !important;
    padding: 0 !important;
  }

  code.hljs {
    text-align: left;
    padding: 15px !important;
    margin: 0 !important;
  }
</style>