<template>
  <div class="avatar">
    <b-img rounded="circle" :src="imgSrc"/>
  </div>
</template>

<script>

export default {
  props: {
    src: { type: String },
    title: { type: String }
  },
  computed: {
    imgSrc () {
      return typeof this.src === 'undefined' || this.src.length === 0 ? '/img/default-avatar.jpg' : this.src
    }
  }
}
</script>

<style lang="scss" scoped>
  .avatar {
    position: relative;
    font-size: 3em;
    width: 1em;
    height: 1em;
    border-radius: 50%;
    background-color: #999;

    > img {
      position: absolute;
      width: 100%;
      height: 100%;
    }
  }
</style>
