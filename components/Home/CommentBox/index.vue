<template>
  <div class="comment-txt">
    <h2 class="head-title">Comment Here</h2>
    <div class="cmt-txt">
      <textarea
        type="text"
        placeholder="Add Comment.."
        v-model="comment"
        @keypress="keydown"
        v-bind:class="error==true?'error':''"
        maxlength="200"
      ></textarea>
      <input type="button" value="Submit" v-on:click="adddata" />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      comment: "",
      error: false
    };
  },
  methods: {
    adddata() {
      if (this.comment != "") {
        this.$emit("click", this.comment);
        this.comment = "";
      } else {
        this.error = true;
      }
    },
    keydown() {
      this.error = false;
    }
  }
};
</script>