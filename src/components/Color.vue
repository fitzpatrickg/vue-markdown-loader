<template>
  <div class="color-container">
    <div class="show-color" style="background-color: #1a1a1a">

    </div>
    <span class="d-block">Name: {{ name }}</span>
    <span class="d-block">Hex Code: {{ hex }}</span>
  </div>
</template>

<script>
export default {
  name: 'Color',

  props: ['name', 'hex'] 
}
</script>

<style scoped>
.color-container {
  width: 200px;
  text-align: center;
  float: left;
  margin: 25px;
}

.show-color {
  margin-bottom: 12px;
  border-radius: 100px;
  width: 200px;
  height: 200px;
}
</style>