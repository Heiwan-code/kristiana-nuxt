<template>
  <div>
    <BasicCalculator></BasicCalculator>
    <!-- <PrimaryGallery class="home-gallery" id="bestGallery" :imgz="gallery01" :maxImageCount="2"></PrimaryGallery>
    <PrimaryGallery class="home-gallery" id="bestGallery" :imgz="gallery02" :maxImageCount="5"></PrimaryGallery>
    <PrimaryGallery class="home-gallery" id="bestGallery" :imgz="gallery01" :maxImageCount="8"></PrimaryGallery> -->
  </div>
</template>

<script>

export default {
  data () {
    return {
      gallery01: [
        'c.png', 'a.png', 'd.png', 'c.png', 'a.png', 'c.png', 'a.png', 'c.png', 'a.png', 'd.png', 'c.png', 'a.png', 'c.png', 'a.png'
      ],
      isAdmin: false
    }
  },
  mounted () {
    // console.log(this.gallery01)
    // console.log(this.gallery01)
  },
  methods: {
    sortByAlphabet (list) {
      list.sort((a, b) => a.localeCompare(b))
    }
  }
}
// sortByAlphabet(gallery01)

</script>
