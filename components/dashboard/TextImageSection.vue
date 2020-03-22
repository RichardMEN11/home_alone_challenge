<template>
  <b-container class="my-5 py-5">
    <b-row>
      <b-col md="7" order-sm="1" :order-md="imgPos === 'left' ? '2': '1'" :offset-md="imgPos === 'left' ? '1' : '0'">
        <h2 class="mt-5 py-auto">
          {{ heading[0] }}  <span class="highlighted">{{ heading[1] }}</span>
        </h2>
        <p class="index--paragraph pt-4">
          {{ text }}
        </p>
      </b-col>
      <b-col md="4" :offset-md="imgPos === 'left' ? '0' : '1'" order-sm="1" :order-md="imgPos === 'left' ? '1': '2'">
        <b-img :src="imgLink" fluid alt="Responsive image" />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  props: {
    heading: {
      type: Array,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    imgLink: {
      type: String,
      required: true
    },
    imgPos: {
      type: String,
      default: 'left'
    }
  }
}
</script>

<style lang="scss" scoped>
.index{
      &--paragraph{
      font-size: 18px;
      line-height: 30px;
    }
}
</style>
