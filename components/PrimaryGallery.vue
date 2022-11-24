<template>
  <div class="gallery">
    <!-- <SimpleImageWrapper v-for="(img, index) in galleryImgs" :key="index" :imgSource="img" > -->
    <!-- </SimpleImageWrapper> -->
  </div>
</template>

<script>
export default {
  data () {
    return {
      minImageCount: 1
    }
  },
  props: {
    imgz: {
      Type: Array,
      default: []
    },
    maxImageCount: {
      Type: Number,
      default: 0
    }
  },
  computed: {
    galleryImgs () {
      // imgz = 'c.png', 'a.png', 'd.png', 'c.png', 'a.png', 'c.png', 'a.png'
      // maxImageCount = 3
      let sliceTo = this.minImageCount
      if (this.maxImageCount > sliceTo) {
        sliceTo = this.maxImageCount
      }
      return this.imgz.slice(0, sliceTo)
    }
  },

  methods: {
    // addRandomHash (name) {
    //   var result           = '';
    //   var characters       = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
    //   var charactersLength = characters.length;
    //   for ( var i = 0; i < length; i++ ) {
    //       result += characters.charAt(Math.floor(Math.random() * charactersLength));
    //   }
    //   return name + '_' + result;
    // }
  }
}
</script>
