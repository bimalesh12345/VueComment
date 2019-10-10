<template>
  <div class="comment-box">
    <div class="commentbox">
      <CommentBox @click="addList($event)" />
      <CommentList :list="list" :color="color" />
    </div>
  </div>
</template>
<script>
import CommentBox from "./CommentBox/index.vue";
import CommentList from "./CommentList/index.vue";
export default {
  components: { CommentBox, CommentList },
  data() {
    return {
      list: [],
      color: []
    };
  },
  methods: {
    addList(val) {
      if (val != "") {
        this.list.push(val);
        random_bg_color(this);
      } else {
      }
    }
  }
};
function random_bg_color(_this) {
  var x = Math.floor(Math.random() * 256);
  var y = Math.floor(Math.random() * 256);
  var z = Math.floor(Math.random() * 256);
  var bgColor = "rgba(" + x + "," + y + "," + z + ",.5)";
  console.log(bgColor);
  _this.color.push(bgColor);
}
</script>