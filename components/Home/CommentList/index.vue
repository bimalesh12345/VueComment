<template>
  <div class="cooment-msg">
    <ul>
      <coment-list v-for="(li, index) in list" :key="index" :li="li" :color="color" :index="index"></coment-list>
    </ul>
  </div>
</template>
<script>
import ComentList from "./ComentList.vue";
export default {
  props: ["list", "color"],
  components: { ComentList }
};
</script>