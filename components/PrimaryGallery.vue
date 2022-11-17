<template>
  <div class="gallery">
    <SimpleImageWrapper v-for="(img, index) in imgz" :key="index" :imgSource="img"></SimpleImageWrapper>
  </div>
</template>

<script>
export default {
  props: {
    imgz: {
      Type: Array,
      default: []
    }
  }
}
</script>
