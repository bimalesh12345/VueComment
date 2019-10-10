<template>
  <li v-bind:style="{'background-color': color[index]}">
    <h3>Bimal</h3>
    <p>{{li}}</p>
  </li>
</template>
<script>
export default {
  props: ["li", "color", "index"]
};
</script>