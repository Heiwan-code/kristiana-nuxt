<template>
  <div class="image-wrapper">
    <img :src="require(`@/assets/images/${imgSource}`)" alt="">
  </div>
</template>

<script>
export default {
  props: {
    imgSource: {
      Type: String,
      default: null
    }
  }
}
</script>
